# Intro to JavaScript Modules
JavaScript modules are reusable pieces of code that can be exported from one program and brought into another program. Modules are particularly useful for a number of reasons:
- Maintainability: Modules can be updated individually without affecting other parts of the codebase.
- Namespace: Variables defined inside a module won't conflict with those in another module or global scope.
- Reusability: Functions defined in a module can be reused across different parts of your application.

# Exporting Modules: Named
In JavaScript, you can export functions, objects, or primitive values from a module so that they can be used by other scripts.

```javascript
// math.js
export const add = (a, b) => a + b;
export const subtract = (a, b) => a - b;
```
In the above example, `add` and `subtract` are named exports from the `math.js` module. These can be imported in other modules using their names.

# Exporting Modules: Default
If a module is designed to export a single value or object, we can use the default export. 

```javascript
// person.js
export default class Person {
  constructor(name) {
    this.name = name;
  }
}
```
In the above example, `Person` class is the default export from `person.js`. When importing a default export, you don't need to use curly brackets and you can name it whatever you want.

# Exporting Modules: Multiple
You can also export multiple items from a module. These items can be a mix of named and default exports.

```javascript
// utils.js
export const helperFunc1 = () => {};
export const helperFunc2 = () => {};
export default () => {
  // default function...
};
```
In the above example, `helperFunc1` and `helperFunc2` are named exports and the unnamed function is the default export from the `utils.js` module.

# Renaming Imported Modules
When importing named exports, you can rename them using the `as` keyword. This can be useful to avoid naming conflicts with local variables.

```javascript
import { helperFunc1 as utilityFunc1, helperFunc2 as utilityFunc2 } from './utils.js';
```
In the above example, `helperFunc1` and `helperFunc2` are renamed to `utilityFunc1` and `utilityFunc2` respectively in the local scope.

Remember that renaming isn't possible with default imports as you can give any name you want during default import. Also, you can combine default and named imports in a single import statement.

```javascript
import defaultExport, { namedExport as Alias } from './module.js';
```

In the above example, `defaultExport` is the default export from the `module.js` and `namedExport` is the named export which has been renamed to `Alias` in the local scope.
