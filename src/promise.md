# 🚀JavaScript Promises

A Promise is a JavaScript object that represents the future result of an asynchronous operation. It can be in one of three states:

- Pending (initial)

- Fulfilled (operation successful)

- Rejected (operation failed)


### 🛠 Promise Syntax:
The constructor syntax for a promise object is:
```js
  let promise = new Promise(function(resolve, reject) {
     // async operation
})

// Example
 let promise = new Promise((resolve, reject) => {
  setTimeout(() => resolve("Done!"), 2000);
});
```

---

### ➕then(), catch(), finally()

This is used to handle the result of the promise.

```js
promise
  .then((result) => console.log("Success:", result)) // on resolve
  .catch((error) => console.log("Error:", error))    // on reject
  .finally(() => console.log("Finished!"));          // always
```

### ❓Why Use Promises?

- Better error handling

- Avoids callback hell - before we use nested callbacks

- Promises make async code cleaner and easier to manage