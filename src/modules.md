# Modules

<!-- kareemah here  -->
# What are Modules in Javascript?
- Javascript modules are simply files that uses special directives Import & Export
- JavaScript modules let you **split your code** into separate files.
- You can **import** and **export** parts of code.
- Helps keep code **organized** and **reusable**.

## Why Use Modules?

- Makes your code cleaner
- Easier to debug
- Reuse code in multiple places
- Collaborate better in teams

---

### You can import and export things like:
- Variables
- Functions
- Classes

## Importing

import { greet } from './greet.js';

console.log(greet('Alice')); // Hello, Alice!


## Exporting 


// greet.js

export function greet(name) {
  return `Hello, ${name}!`;
}



<!-- Uzoma here  -->