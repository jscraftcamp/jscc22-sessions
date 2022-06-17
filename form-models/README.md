# Form Models

Forms models are a way to further define your specs. he purpose lies in having all the possible values of a form reflected as model definition. The form model then gets mapped to or from the regular domain models using mapper functions. These mapper functions would adjust for any differences.

![Whiteboard Photo](https://pbs.twimg.com/media/FVcydoXWYAA5zFI?format=jpg&name=large)

## Use Case

If you have a single page application (SPA) that manages lots of data locally (while synchronizing with the BE in the background), the you want to have your form data sanitized before sending to the BE. This is beneficial for the UX because there is no need to wait for the BE to return corrected data, the application has a real-time characted.

## Benefits

### Contain Form Changes

The basic idea is to separate the view-related form area from the domain area within a FE. So, i.g. when the domain model changes from the BE side, the FE domain model needs to be updated as well but it should not automatically mean that the form controls need to be changed in consequence. Instead, the change would be contained until the mapping function (doain model -> form model), while the form handling remains unchanged.

### Contain BE Changes

Or, if the form changes, maybe a different component library is used that handles values differently, such changes could be contained within the form models, up to the mapping function, leaving the domain models untouched.

### Reflect typing differences

Maybe a component library provides data types that are incompatible with the BE, i.g. in a form model you may need a `Moment` object, while the BE processes `string` representation of a date.

Maybe you are using a custom object type on the FE, i.g. coordinates, while the BE maybe uses from a standard library.

Maybe the form values nullability is not 100% compatible with the nullability on the BE.

### Reflect Split Forms

Sometimes, domain models are large and require to be split into several forms. The form models would then reflext each individual form.

## Implementation Example

Define FORM MODELS types with Typescript. You can map the form and domain model to avoid collisions and to make changes, if the backend model needs the data in a specific format.

```ts
export interface PersonFormModel {
  name?: string; // disabled angular form controls return undefined
  age?: moment.Moment; // a component library may provide special data types
}

export interface Person {
  name: string | null; // non-undefined because the field must exist, but accepts null values
  age?: string; // standard ISO date string
}

export function fromPersonFormModel(value: PersonFormModel): Person {
  return {
    name: value.name ?? null,
    age: value.age != null ? value.age.format("YYYY-MM-DD") : undefined,
  };
}

export function toPersonFormModel(value: Person): PersonFormModel {
  return {
    name: value.name ?? undefined,
    age: moment(value.age), // also make sure you handle incorrect values and exceptions
  };
}
```
