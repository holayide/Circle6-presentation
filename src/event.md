# Events

<!-- innocent here  -->

---

title: Understanding EventListeners in JavaScript
subtitle: Learn with Simple Examples

---

# What is an EventListener?

An **EventListener** is like telling the computer:

> “**When** something happens (like a click, hover, or key press), do this action.”

---

# Example

Imagine your light switch at home.
You (user) flip it (event), and the light turns on or off (action).

# Basic Format

```js
// Syntax
element.addEventListener("event", function);
```

- `element` — the HTML element (e.g., button)
- `"event"` — like `"click"`, `"keydown"`, etc.
- `function` — the action to perform

---

# Example 1: Click a Button

```html
<button id="myButton">Click me!</button>
<script>
  document.getElementById("myButton").addEventListener("click", function () {
    alert("You clicked the button!");
  });
</script>
```

---

# Example 2: Change Text on Click

```html
<button id="changeBtn">Change Text</button>
<p id="myText">Hello!</p>
<script>
  document.getElementById("changeBtn").addEventListener("click", function () {
    document.getElementById("myText").textContent = "Text changed!";
  });
</script>
```

---

# Summary

Think of addEventListener like telling the browser:

“When this happens, do that.”

Events you can listen for:

click, mouseover, mouseout, keydown, keyup, submit, dblclick
and many more!

- EventListeners wait for things to happen (clicks, keys, etc).
- Use `element.addEventListener("event", function)`
- Works with any HTML element
