# Callback Function
# Introduction to Callbacks

A **callback** is a function passed as an argument to another function.  
It's often used to handle **asynchronous operations** like API calls, timers, or events.


## 📦 Why Use Callbacks?                         
- Handle async code in a structured way              
- Ensure a task runs *after* something else finishes 
- Enable flexible and reusable functions  

## 💡 Basic Example
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