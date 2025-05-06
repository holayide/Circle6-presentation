# 🚀EventListener

An **EventListener** lets your webpage respond to user actions, like clicks, key presses, or mouse movements.

> “**When** this happens, do that”


### 🔧 Syntax:

```js
element.addEventListener("event", function);
```

- `element` — the HTML element (e.g., button)

- `"event"` — like `"click"`, `"keydown"`, etc.

- `function` — what to do when the event happens

---

### ✏️ Examples:

```html
<!-- click event -->
<button id="myButton">Click me!</button>

<script>
  document.getElementById("myButton").addEventListener("click", function () {
    alert("You clicked the button!");
  });
</script>


<!-- Mouseover Event -->
<input type="text" id="nameInput" placeholder="Hover over me" />

<script>
  document.getElementById("nameInput")
    .addEventListener("mouseover", function () {
      console.log("Mouse is over the input!");
    });
</script>
```