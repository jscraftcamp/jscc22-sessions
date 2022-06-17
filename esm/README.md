# ES Modules 

- History of CommonJs Modules / ES Modules 
  - Timeline: script tags - ES 2015 - import (defering, async)
  - Requirejs did what import statements do now
  - bundlers came in to handle hte imports - now UMD to work across all platforms (UMD important for platform developers)

Random Notes

- bundler handle treeshaking

- Node is now using ESM experi

- old: require (CommonJs); new: import (ESM)

- [Blog Article of Sindre Sorhus](https://medium.com/sindre-sorhus/hello-modules-d1010b4e777b)

- [JSON Import](https://github.com/tc39/proposal-json-modules#synopsis)

- strict mode is not automatic

  - if you use `type: module` esm is enabbled (`.js` files are handled as `.mjs`then - `require` will not be accepted anymore)

  - [hack: switch to `type: module` *if possible*](https://github.com/tc39/proposal-json-modules#synopsis): (this reduces bundle size by a lot)

    ```html
      <script type="module" src="https://www.....js" async defer></script>
      <script nomodule src="https://www.....js" async defer></script>
    ```

  - ...adapt webpack tooling to do 2 bundles to achieve that

- how is everyone doing/dealing with these kind of breaking changes of ESM?

- opinions on esbuild 

  - good to strip away the types of typescript and serve modules
  - used by vite (esbuild is just super fast... but overpromises?)

- 
