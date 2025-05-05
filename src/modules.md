# Modules

<!-- kareemah here  -->
# What are Modules in Javascript?
- Javascript modules are simply files that uses special directives Import & Export
- JavaScript modules let you **split your code** into separate files.
- You can **import** and **export** parts of code.
- Helps keep code **organized** and **reusable**.

## Why Use Modules?

- Makes your code cleaner
- Easier to debug
- Reuse code in multiple places
- Collaborate better in teams

---

### You can import and export things like:
- Variables
- Functions
- Classes

## Importing
```ts {all|5|7|7-8|10|all} twoslash
// main.js
import { greet } from './greet.js';

console.log(greet('Alice')); // Hello, Alice!

```

## Exporting 
```ts {all|5|7|7-8|10|all} twoslash

// greet.js
export function greet(name) {
  return `Hello, ${name}!`;
}
```



<!-- Uzoma here  -->
# What is Module?

Module is just a separate file that contains some javascript codes like functions, variables etc, that you can reuse in other files.

# Types of modules
ECMAScript Modules (Use Export and Import)

CommonJS Modules (Use modules.export and require)

# Why Use Modules?

It Organizes your code into reusable files.

It Keeps code clean and maintainable.

Enable lazy loading.

Easy testing.

Avoid global variables.


---
transition: slide-up
level: 2
---

# For example, this is Fitness App using modules.


```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Fitness Tracker</title>
</head>
<body>
  <h1>Fitness Tracker 🏋️</h1>
  <input type="text" id="exerciseInput" placeholder="Exercise name (e.g., Push-ups)" />
  <input type="number" id="countInput" placeholder="Count (e.g., 20)" />
  <button id="addWorkoutBtn">Add Workout</button>

  <h2>Workout Log:</h2>
  <ul id="workoutList"></ul>

  <script type="module" src="main.js"></script>
</body>
</html>

```

---

 For instance, if we have a file `workoutData.js` and `ui.js` exporting a function:


```js
// 📁 workoutData.js 
// Manages the workout data
export const workouts = [];

export function addWorkout(name, count) {
  workouts.push({ name, count, date: new Date() });
}
```

```js
// 📁 ui.js
// Handles updating the UI
export function renderWorkouts(workouts) {
    const list = document.getElementById('workoutList');
    list.innerHTML = ''; // Clear list
  
    workouts.forEach((workout, index) => {
      const li = document.createElement('li');
      li.textContent = `${index + 1}. ${workout.name} - ${workout.count} reps (${workout.date.toLocaleDateString()})`;
      list.appendChild(li);
    });
  }
  
  export function clearInputs() {
    document.getElementById('exerciseInput').value = '';
    document.getElementById('countInput').value = '';
  }
  
```
---

```js
// 📁 main.js 
import { addWorkout, workouts } from './fitness/workoutData.js';
import { renderWorkouts, clearInputs } from './fitness/ui.js';

const addBtn = document.getElementById('addWorkoutBtn');
const exerciseInput = document.getElementById('exerciseInput');
const countInput = document.getElementById('countInput');

addBtn.addEventListener('click', () => {
  const name = exerciseInput.value.trim();
  const count = Number(countInput.value);

  if (!name || !count || count <= 0) {
    alert('Please enter a valid exercise and count!');
    return;
  }

  addWorkout(name, count);
  renderWorkouts(workouts);
  clearInputs();
});

```

