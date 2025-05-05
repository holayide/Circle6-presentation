# 🚀Callback Functions

- A **callback** is a function passed into another function as an argument. 
- Commonly used to handle **asynchronous operations** like API calls, timers, or event handling.


## 📦 Why Use Callbacks?                         
- Run code after a task finishes (e.g., after a response).

- Helps write non-blocking, cleaner async code.

- Makes functions more flexible and reusable. 

---

## ✏️ Examples:
```js
function greet(name, callback) {
  console.log("Hi " + name);
  callback();
}

function sayBye() {
  console.log("Goodbye!");
}

greet("Ada", sayBye);
// Output:
// Hi Ada
// Goodbye!
```