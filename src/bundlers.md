# 🚀Bundlers


### 🔹 What are Bundlers?

Bundlers are tools that combine and optimize multiple files (JavaScript, CSS, images, etc.) into a single output (or smaller, optimized ones).


### 🔹 Why Use Bundlers?

Since ES modules in browsers are not fully supported yet and have several limitations, build tools help resolve these issues. For example, they allow us to handle things like importing media files, which isn’t natively supported by the browser's module system.

---

### 🔹 Popular Bundlers

- Webpack – Flexible, most commonly used for JavaScript apps

- Parcel – Zero-config bundler, good for small projects

- Rollup – Focused on efficient bundling for libraries


### ✏️ Example:  (vite install)

```bash 
# 1. Create a new Vite project (React example)
npm create vite@latest my-app -- --template react

# 2. Navigate to project
cd my-app

# 3. Install dependencies
npm install

# 4. Run dev server (blazing fast ⚡)
npm run dev
```