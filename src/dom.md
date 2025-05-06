# 🚀Broswer Environment(Dom, Bom, Cssom)

### 🟦 DOM – Document Object Model

- Interface between JavaScript & HTML/CSS

- JavaScript lets us modify the DOM, and this process is called **DOM Manipulation**.

- JavaScript interacts with the DOM through:
    * HTML attributes (e.g. `onclick="..."`)
    * DOM properties (e.g. `element.textContent = "Hi"`)
    * Event listeners (e.g. `element.addEventListener("click", ...)`)

- Methods to access the elements include: `getElementById()`, `querySelector()` et.c

```js
// Change text in a heading
document.getElementById("title").textContent = "Welcome!";
```

---

### 🟨 BOM – Browser Object Model

- Interface between JavaScript & Browser

- The BOM provides access to the browser's functionality, such as interacting with the window, location, and history.

```js
// Redirect to a new URL
location.href = "https://wikipedia.org";
```

### 🟩 CSSOM – CSS Object Model

-  Interface between JavaScript & CSS

- The CSSOM allows JavaScript to interact with the CSS, letting you manipulate styles dynamically.

```js
// Change color of an element
document.querySelector("h1").style.color = "red";
```