**Building a Math Module**: 
   - **Prompt**: Create a JavaScript file named `math.js`. This module should export four functions: `add()`, `subtract()`, `multiply()`, and `divide()`, each performing the respective mathematical operation. In a separate JavaScript file, import these functions and use them to perform some calculations.
   - **Hint**: Use named exports to export functions from the `math.js` module and remember to import these functions using their correct names in the other file.

**Creating a Personal Information Module**: 
   - **Prompt**: Develop a module named `person.js`. This module should have a default export of a `Person` class with properties `name`, `age`, and `location`. Also, add a named export `greet()` function that logs a greeting to the console. Import this module in another JavaScript file and use the `Person` class and `greet()` function.
   - **Hint**: When importing the `Person` class (a default export), you can name it anything you like. But, you need to import `greet()` with its specific name.
     
**Renaming on Import**: 
   - **Prompt**: Create a module that exports a few functions or variables. In another JavaScript file, import these functions or variables but rename them upon import. Use these renamed functions or variables in your code.
   - **Hint**: Use the `as` keyword to rename imports. For instance, `import { originalName as newName } from './module.js';`
