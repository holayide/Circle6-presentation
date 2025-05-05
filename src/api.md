# 🚀Application Programming Interface(API)

### 🔹What is API?

- It lets applications communicate with each other

- Acts as a bridge between frontend and backend or between different services


### Web APIs?

- A Web API sends or receives data over the internet
- Uses URLs and methods like: 
  * `GET` – get data
  * `POST` – send new data
  * `PUT` – update data
  * `DELETE` – remove data

---

### How a Web API Works

- You send a request to an API URL (called an endpoint)
- The server processes it
- You get a response (usually in JSON format)

### Example:

```js
fetch('https://api.agify.io?name=Tawakalt')
  .then(res => res.json())
  .then(data => console.log(data));

// Response
// {
//   "name": "Maryam",
//   "age": 22,
//   "count": 12000
// }
```

Tools: Postman, RapidAPI et.c






