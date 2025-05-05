# React JS: Introduction & Overview

- React is a **JavaScript library** created by Facebook and is used to build **fast, interactive user interfaces**.
- It’s one of the most used JavaScript libraries and ideal for **single-page applications** (SPAs).

🗂️ A **Single Page Application (SPA)** loads one HTML page and dynamically updates content without reloading the page.

 **Components in React**

- React apps are made up of **components** — independent and reusable UI pieces combined to build complex interfaces.
- Every app starts with a **root component**, that holds all other components.

---

# ⚙️ How React Works

🔧 A React component is just a **JavaScript function** that returns **JSX**.

Example:
```jsx
function Greeting({ name }) {
  return <h1>Hello, {name}!</h1>;
}
```

- **JSX** is a syntax extension that lets you write HTML-like code inside JavaScript.
- **Props** are React's way of passing information from one component to another.

---

 Behind the scenes, React optimizes how changes appear on the screen using the **Virtual DOM**.

- Updating the browser’s **real DOM** directly is slow.
- React uses a **Virtual DOM** — a lightweight copy of the real DOM — to make updates more efficient.

Here’s how it works:
1. React builds a **new Virtual DOM** when the UI changes.
2. It compares this with the previous Virtual DOM (this process is called **diffing**).
3. React identifies what has changed.
4. It updates **only the changed parts** in the real DOM — not the whole page.

---

#  Why React?

-  **Reusable components** save time and reduce repetition.
-  **Fast rendering** using the Virtual DOM improves performance.
-  **Modular architecture** makes code easier to maintain and scale.
-  Backed by **a large community** and used by companies like Facebook, Instagram, Netflix.
-  Works well with modern development tools and libraries.

React is popular not just because it’s powerful — but because it makes building complex apps simpler and more efficient.
