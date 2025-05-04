# Application Programming Interface(API)

<!-- Tawakalitu here  -->

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





