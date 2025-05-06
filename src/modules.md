# 🚀JavaScript Modules (ES Modules)

### What are Modules?
- A module is a JavaScript file that exports code (like functions or variables) for use in other files.
- Modules use **export** and **import** statements.
- Helps split code into reusable, organized chunks.

### Ways to import/export within modules

- Named Export/Import - e.g `import { name, func } from './module'`;
- Default Export/Import - e.g `export default function() {}`;
- Renaming - e.g `import { name as localName } from './module'`;
- Namespace Import (*) - e.g `import * as module from './module'`;
- Dynamic imports - e.g `const module = await import('./module')`;

---

### What Can You Export?
- Variables
- Functions
- Classes


### ✏️ Examples:
```js 
// named export
export function greet(name) {

  return `Hello, ${name}!`;

}


// named import
import { greet } from './greet.js';

console.log(greet('Alice'));
// Hello, Alice!
```