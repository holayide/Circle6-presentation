# 🚀React JS: Introduction & Overview

- React is a **JavaScript library** created by Facebook and is used to build **fast, interactive user interfaces** especially single-page applications (SPAs).

### Core Concepts in React

- components — independent and reusable UI pieces combined to build complex interfaces.
- JSX(Javascript xml) - helps to write HTML-like syntax in JavaScript for React components. JSX has 3 important rules which are:

      * must return a single root element (must be wrapped in `<div> or <></>`)
      * all tags must be closed (e.g ,`<input>` )
      * camelcase should be used for most of the things(e.g, `className`)

---

## ✏️ Examples:
```jsx
function Greeting({ name }) {
  return <h1>Hello, {name}!</h1>;
}

function WelcomeMessage({ name }) {
  return (
    <>
      <h1>Hello, {name}!</h1>
      <input type="text" />
    </>
  );
}
```

---

## Why React?

- Reusable components — save time and reduce repetition.
- Fast rendering — using the Virtual DOM improves performance.
- Simple and Less opinionated — its lightweight.
- Popular — strong community support.
- Flexibility — its  allows developers to build applications the way they want.
