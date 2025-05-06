# React JS: Introduction & Overview

- React is a **JavaScript library** created by Facebook and is used to build **fast, interactive user interfaces**.
- It’s one of the most used JavaScript libraries and ideal for **single-page applications** (SPAs).

 **Components in React**

- React apps are made up of **components** — independent and reusable UI pieces combined to build complex interfaces.
- Every app starts with a **root component**, that holds all other components.

🔧 A React component is just a **JavaScript function** that returns **JSX**.
  - **JSX** is a syntax extension that lets you write HTML-like code inside JavaScript.

---

Example:
```jsx
function Greeting({ name }) {
  return <h1>Hello, {name}!</h1>;
}
```
  # ⚙️ How React Works

- React uses a **Virtual DOM** — a lightweight copy of the real DOM — to make updates more efficient.

When the UI changes, React first builds a new Virtual DOM. It then compares it to the previous version. After identifying what has changed, React updates only the affected parts of the real DOM, making the update efficient and fast.


---

#  Why React?

-  **Reusable components** save time and reduce repetition.
-  **Fast rendering** using the Virtual DOM improves performance.
-  **Modular architecture** makes code easier to maintain and scale.
-  Backed by **a large community** and used by companies like Facebook, Instagram, Netflix.
-  Works well with modern development tools and libraries.