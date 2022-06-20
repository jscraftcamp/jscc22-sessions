# React component library

**Session by Jörn**

Instead of creating your own component library, you could provide a theme for Matial UI. In earlier versions though, teams could have issues with performance.

Constraints can be a good thing, users don't really need full flexibility.

A big question is how to sync all the people (designer of the app, developer of the app, developer of the component library, designer of the component library)?

Everyone needs to be reusing the "atomics" -> Atomic Design. Start from very basic building blocks.

It's faster for all if the design system is constrained and everybody knows that (starting from the designers).

1. How to forward props to the root element?

- Would you give the flexibility of the root element to the user or wouldn't you?
  You may not want to have the root element clickable.

2. How to check whether the API is "good enough"?

3. TypeScript write propTypes for us?

Example of good constraint for the component library:

```
Base button:
 --------
| Button |
 --------

No:
 --------
|        |
| Button |
|        |
 --------

No:
 ----------------
|     Button     |
 ----------------

YES (ratios stay the same):
 ----------------
|                |
|     Button     |
|                |
 ----------------
```
