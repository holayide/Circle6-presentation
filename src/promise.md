# JavaScript Promise


At the core, a Promise in JavaScript is just an object that represents a value that will be available later.
Not immediately — later.

This a simple example of a promise. 
A promise is an object that represents the eventual completion (or failure) of an asynchronous operation and its resulting value. It allows you to write cleaner and more manageable code when dealing with asynchronous operations, such as API calls, file reading, or timers.

---

The constructor syntax for a promise object is:
```js
  let promise = new Promise(function(resolve, reject) {
    //executor
})
```
The function passed to new Promise is called the executor. When new Promise is created, the executor runs automatically. It contains the producing code which should eventually produce the result.
It's arguments (resolve, reject) are callbacks provided by JavaScript itself. Our code can call resolve when the job is done successfully, and reject if an error happened. The difference between them is that resolve is called when the promise is fulfilled, and reject is called when the promise is rejected. Our code is only inside the executor.

When the executor obtains the result, be it soon or late, doesn’t matter, it should call one of these callbacks:

resolve(value) — if the job is finished successfully, with result value.

reject(error) — if an error has occurred, error is the error object.

---

The new Promise constructor returns a promise object, which is in the pending state. The promise can be in one of three states:

1.State — initially "pending", then changes to either "fulfilled" when resolve is called or "rejected" when reject is called.

2.result — initially undefined, then changes to value when resolve(value) is called or error when reject(error) is called.

```js
let pour = new Promise(function(resolve, reject) {
     resolve(123)
})
```

A promise that is either resolved or rejected is called "settled", as opposed to an initially "pending" promise. A settled promise can be in one of two states: "fulfilled" or "rejected".
---


## then, catch :

A promise object serves as a link between the executor and the code that uses the result of the promise. The then method is used to handle the result of a fulfilled promise, while the catch method is used to handle the result of a rejected promise. The then method takes two arguments: a callback function to handle the resolved value and an optional callback function to handle the rejected value. The catch method takes one argument: a callback function to handle the rejected value.

The then method returns a new promise, which allows for chaining multiple then calls together. This is useful for handling multiple asynchronous operations in a clean and readable way. The catch method also returns a new promise, which allows for error handling to be chained as well.

```js
let pomp = new Promise( (resolve,reject) => {
    setTimeout(() => resolve("Resolved!"), 2000);
})
pomp.then(function(msg) {
    console.log(msg)
})

```
---

Basically, the then() method is used for when the promise is resolved successfully and the catch() method is used for when the promise is rejected.

 ```js
 let num = 10;
let pour = new Promise(( resolve, reject) => {
    setTimeout(() =>{
        if(num > 12) {
            resolve('Number is greater than 12!')
        } else {
            reject('Number less than 12!')
        }
    }, 2000)
})
pour
.then(function (result) {
    console.log('Success:', result)
})
.catch(function(result) {
    console.log('Error:', result)
})
 ```
 ---

 # finally()
 The finally() method is used to execute a block of code after the promise has been settled, regardless of whether it was resolved or rejected. This is useful for performing cleanup tasks or updating the UI after an asynchronous operation has completed. The finally() method does not take any arguments and does not affect the result of the promise chain.
 Think of it like the cleanup block.
 ```js
 function getStatus() {
    return new Promise( (resolve, reject) => {
        setTimeout(() => {
            const Data = Math.floor(Math.random() * 2);
            console.log(Data)

            const success = Data > 0.5;
            if(success) {
                resolve("✅Data fetched successfully!")
            } else{
                reject("❌ Failed!")
            }
        }, 2000)
    })
}
console.log("⏳ fetching..")
getStatus()
.then((data) => {
    console.log(data)
})
.catch((err) => {
    console.warn(err)
})
.finally(() => {
    console.log("🔚 Task completed!")
})
 ```
---

# Why Use Promises?

 1.Handles Asynchronous Code in a Cleaner Way
Without Promises, you'd rely on nested callbacks (aka "callback hell") which quickly become hard to read and maintain.

Before(callback style):
```js
getUser((user) => {
  getPosts(user, (posts) => {
    getComments(posts, (comments) => {
    });
  });
});

```

  2.Built-in Error Handling
Promises give you a centralized way to catch errors using .catch() — no need to handle errors in every single callback.

With Promises:
```js
getUser()
  .then(getPosts)
  .then(getComments)
  .then((comments) => {
  });

```

<!-- Osamudiameh here  -->