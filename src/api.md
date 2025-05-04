# Application Programming Interface(API)

<!-- Tawakalitu here  -->

---
# API
theme: Seriph
---

# What is API?

API means Application Programming Interface.
"Application" is any software (web app, mobile app, etc.).
"Interface" is how you communicate with that application
API are are responsible for taking in requests, talking to the system (server), and bringing back results.

---


# Why Do We Use APIs?

- To reuse code or services (like Google Maps, Payment Gateways, etc.)

- To access features or data from other apps (e.g., weather, news, etc.)

- To connect frontend to backend in web development

---

transition: slide-up
level: 2

---

# Types of APIs

- Web APIs (most common) – use HTTP protocol.

- Library APIs – used within software libraries (like Python’s math module).

- Operating System APIs – let apps interact with OS (like Windows or Android).

- Hardware APIs – control devices (like camera, Bluetooth, etc.).

  **Lets focus on Web APIs here.**

## What is a Web API?

A Web API is a way for a website or app to get or send data from/to a server using a URL and HTTP methods like `GET`, `POST`, `PUT`, and `DELETE`.

---

# What Does a Web API Consist Of?

1. **Endpoint (URL)** – The address where you send the request
   e.g., `https://api.example.com/users`

2. **HTTP Method** – Types of request includes:

- `GET` – fetch data
- `POST` – create data
- `PUT` – update data
- `DELETE` – remove data

3. **Headers** – Extra information like authentication (API keys, Content-Type)

4. **Request Body** – Data you send (for POST/PUT requests), often in JSON

5. **Response** – What you get back: usually JSON data and a status code

---

transition: slide-up
level: 2

---

# Code Example: Using a Web API (JavaScript + fetch)

```
fetch('https://api.agify.io?name=Tawakalt')
  .then(res => res.json())
  .then(data => console.log(data));
```

This calls the **Agify API** which guesses the age of a person based on their name.

Response

```
{
  "name": "Maryam",
  "age": 22,
  "count": 12000
}
```

---

## level: 2

# Web APIs Authentication

Most API often use:

- API keys

- Bearer tokens (JWT)

- OAuth (used by Google, Facebook, etc.)

---

# Tools to Explore Web APIs

- **Postman** – This allows us test our APIs without writing code

- **RapidAPI** – Allows us find and test APIs

- **Browser Console** – This is for simple GET requests

---

# Here is a Simple App To Solidify Our Knowledge

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Age Guesser</title>
  <style>
    body {
      font-family: sans-serif;
      text-align: center;
      padding: 40px;
    }
    input {
      padding: 10px;
      width: 200px;
    }
    button {
      padding: 10px 15px;
      margin-left: 10px;
    }
    #result {
      margin-top: 20px;
      font-size: 1.2em;
    }
  </style>
</head>
<body>

  <h1>Guess the Age by Name</h1>
  <input type="text" id="nameInput" placeholder="Enter a name" />
  <button onclick="guessAge()">Guess Age</button>
  <div id="result"></div>

<!--JavaScript code starts here-->
<br>
<br>

  <script>
    function guessAge() {
  const name = document.getElementById('nameInput').value;

  if (!name) {
    document.getElementById('result').innerText = 'Please enter a name.';
    return;
  }

  fetch(`https://api.agify.io?name=${name}`)
    .then(res => res.json())
    .then(data => {
      document.getElementById('result').innerText =
        `The guessed age for ${data.name} is ${data.age} years old (based on ${data.count} records).`;
    })
    .catch(error => {
      console.error('Error:', error);
      document.getElementById('result').innerText = 'Something went wrong.';
    });
}

  </script>
</body>
</html>

## Thank You