# React-JS-Tutorial
---

## ✅ **React JS**

**React JS** is a **JavaScript library** used to build **user interfaces** (UI), especially for **single-page applications** where you need fast interactions without reloading the page.

---

## ❓ Why React JS?

React helps developers:

* Create large web apps that can update and render efficiently.
* Reuse components (small blocks of UI).
* Keep code more organized and easier to manage.

---

## 🌟 Advantages of React JS

1. **Component-Based**: Build encapsulated components that manage their own state.
2. **Reusable Code**: Use components again and again.
3. **Virtual DOM**: Makes updates fast and efficient.
4. **Unidirectional Data Flow**: Makes app predictable and easier to debug.
5. **JSX**: Lets you write HTML in JavaScript for easy UI building.

---

## ▶️ Running JavaScript in HTML

We can write JavaScript inside an HTML file using the `<script>` tag:

```html
<!DOCTYPE html>
<html>
<head>
  <title>JavaScript in HTML</title>
</head>
<body>
  <h1>Hello</h1>
  <script>
    alert("This is JavaScript running in HTML!");
  </script>
</body>
</html>
```

---

## 🔨 Creating Elements using React JS

To use React, we can **create elements** that represent DOM nodes.

---

## 📦 React CDN

You can use React by including it via **CDN** in your HTML file.

```html
<!DOCTYPE html>
<html>
<head>
  <title>React via CDN</title>
  <!-- React and ReactDOM -->
  <script src="https://unpkg.com/react@17/umd/react.development.js"></script>
  <script src="https://unpkg.com/react-dom@17/umd/react-dom.development.js"></script>
</head>
<body>
  <div id="root"></div>

  <script>
    // React code will go here
  </script>
</body>
</html>
```

---

## ⚛️ React.createElement()

This function creates a React element.

```js
const element = React.createElement('h1', null, 'Hello, React!');
```

This is similar to writing `<h1>Hello, React!</h1>` but using plain JavaScript.

---

## 🖼️ ReactDOM.render()

This function renders the element into the DOM.

```js
ReactDOM.render(element, document.getElementById('root'));
```

### Full Example:

```html
<!DOCTYPE html>
<html>
<head>
  <title>React.createElement Example</title>
  <script src="https://unpkg.com/react@17/umd/react.development.js"></script>
  <script src="https://unpkg.com/react-dom@17/umd/react-dom.development.js"></script>
</head>
<body>
  <div id="root"></div>

  <script>
    const element = React.createElement('h1', null, 'Hello, React!');
    ReactDOM.render(element, document.getElementById('root'));
  </script>
</body>
</html>
```

---

## 🔤 JSX (JavaScript XML)

JSX lets you write HTML inside JavaScript:

```js
const element = <h1>Hello, JSX!</h1>;
```

But browsers can't understand JSX directly — that’s where **Babel** comes in.

---

## 🧠 Babel

Babel is a tool that **converts JSX** into regular JavaScript code (like `React.createElement()`).

To use Babel with CDN:

```html
<script src="https://unpkg.com/@babel/standalone/babel.min.js"></script>
```

And mark your script type like this:

```html
<script type="text/babel">
  // JSX code here
</script>
```

---

## 💡 Embedding Variables and Expressions in JSX

You can use `{}` to insert JavaScript expressions inside JSX.

```js
const name = "React";
const element = <h1>Hello, {name}!</h1>;
```

---

## 📦 Nesting JSX Elements

You can nest elements just like you would with HTML.

```js
const element = (
  <div>
    <h1>Main Title</h1>
    <p>This is a paragraph.</p>
  </div>
);
```

---

## ✅ Full JSX Example

```html
<!DOCTYPE html>
<html>
<head>
  <title>JSX Example</title>
  <script src="https://unpkg.com/react@17/umd/react.development.js"></script>
  <script src="https://unpkg.com/react-dom@17/umd/react-dom.development.js"></script>
  <script src="https://unpkg.com/@babel/standalone/babel.min.js"></script>
</head>
<body>
  <div id="root"></div>

  <script type="text/babel">
    const name = "React Learner";

    const element = (
      <div>
        <h1>Hello, {name}!</h1>
        <p>This is JSX in action.</p>
      </div>
    );

    ReactDOM.render(element, document.getElementById('root'));
  </script>
</body>
</html>
```

---

Would you like to move on to **components** next or go deeper into these basics?
