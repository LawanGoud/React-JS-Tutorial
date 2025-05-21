# React-JS-Tutorial

---

## ✅ **React JS**

**React JS** is a **JavaScript library** used to build **user interfaces** (UI), especially for **single-page applications** where you need fast interactions without reloading the page.

---

## ❓ Why React JS?

React helps developers:

- Create large web apps that can update and render efficiently.
- Reuse components (small blocks of UI).
- Keep code more organized and easier to manage.

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
const element = React.createElement("h1", null, "Hello, React!");
```

This is similar to writing `<h1>Hello, React!</h1>` but using plain JavaScript.

---

## 🖼️ ReactDOM.render()

This function renders the element into the DOM.

```js
ReactDOM.render(element, document.getElementById("root"));
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
      const element = React.createElement("h1", null, "Hello, React!");
      ReactDOM.render(element, document.getElementById("root"));
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

      ReactDOM.render(element, document.getElementById("root"));
    </script>
  </body>
</html>
```

---

Awesome! Now that you've learned the React basics, let’s go deeper into **Components**, one of the most important concepts in React. We’ll go step by step, covering only what you've listed.

---

## 🧱 Component

In React, a **component** is a **function or class** that returns a UI element (usually written in JSX). It’s like a small, self-contained block of code that you can reuse and combine to build complex UIs.

### Example: A Simple Functional Component

```jsx
function Welcome() {
  return <h1>Hello from a Component!</h1>;
}
```

You can use this component like a custom HTML tag:

```jsx
<Welcome />
```

---

## 📦 Properties (Props)

**Props** are used to pass data **from parent to child components**.

### Example:

```jsx
function Welcome(props) {
  return <h1>Hello, {props.name}!</h1>;
}

// Usage
<Welcome name="Alice" />;
```

Props make components dynamic and reusable.

---

## 🔁 Component is Reusable

You can use the same component multiple times with different props.

```jsx
<Welcome name="Alice" />
<Welcome name="Bob" />
<Welcome name="Charlie" />
```

Output:

```
Hello, Alice!
Hello, Bob!
Hello, Charlie!
```

---

## 🧩 Component is Composable

**Composable** means components can be **combined together** to build larger parts of the UI.

### Example:

```jsx
function Header() {
  return <h1>My Website</h1>;
}

function Footer() {
  return <footer>© 2025 My Website</footer>;
}

function Page() {
  return (
    <div>
      <Header />
      <p>This is the content.</p>
      <Footer />
    </div>
  );
}
```

`Page` is a composition of `Header` and `Footer`.

---

## 🔌 Third-party Packages

React works well with **npm packages** (open-source libraries) that add extra features — like routing, animation, forms, etc.

Example of popular third-party packages:

- `react-router-dom`: for page navigation
- `axios`: for HTTP requests
- `formik` or `react-hook-form`: for forms

You install these using:

```bash
npm install package-name
```

> Example: `npm install react-router-dom`

---

## ⚙️ create-react-app

`create-react-app` is a command-line tool that sets up a React project with all the tools you need (React, Babel, Webpack, etc.).

### Install (once):

```bash
npm install -g create-react-app
```

### Create a new project:

```bash
npx create-react-app my-app
cd my-app
npm start
```

It automatically sets up:

- File structure
- React
- Babel
- Webpack
- Live-reloading dev server

---

## 🧰 Pre-Configured Tools

When using `create-react-app`, it comes with:

1. **Babel** – Converts JSX into JavaScript.
2. **Webpack** – Bundles all your files together.
3. **ESLint** – Checks code quality and errors.
4. **Development Server** – Live reloads your changes.

So you don’t need to configure anything yourself — just write code!

---

### ✅ Summary of What You Now Know:

| Topic                | Description                                |
| -------------------- | ------------------------------------------ |
| Component            | Reusable UI block                          |
| Props                | Data passed to components                  |
| Reusable             | Use the same component with different data |
| Composable           | Combine components together                |
| Third-party Packages | Add features to React app                  |
| create-react-app     | Tool to set up a full React project        |
| Pre-configured Tools | Babel, Webpack, ESLint built-in            |

---

Great! Let’s now explore **Keys**, **Keys as Props**, and build a simple **Users List Application**. This will tie everything together nicely.

---

## 🔑 **Keys in React**

**Keys** help React identify **which items have changed, are added, or removed** when rendering a list of elements.

- They should be **unique** for each item in a list.
- Keys help **optimize performance** during updates.

### ❌ Bad (no keys)

```jsx
const users = ["Alice", "Bob", "Charlie"];

const list = users.map((user) => <li>{user}</li>);
```

⚠️ React will warn you: _"Each child in a list should have a unique 'key' prop."_

---

### ✅ Good (with keys)

```jsx
const users = ["Alice", "Bob", "Charlie"];

const list = users.map((user, index) => <li key={index}>{user}</li>);
```

Even better: use unique IDs (if available) instead of `index`.

---

## 🔄 Keys as Props

Although you use `key` **in JSX**, React does **not** pass `key` as a `prop` to the component automatically.

### Example:

```jsx
function User(props) {
  return <li>{props.name}</li>;
}

const users = ["Alice", "Bob"];

const list = users.map((name, index) => <User key={index} name={name} />);
```

> `User` component gets `name` prop, but **not** `key`.

If you really need the key value inside the component, you must **pass it manually** as a separate prop:

```jsx
<User key={index} id={index} name={name} />
```

---

## 👥 Users List Application (Step-by-Step)

Let’s build a **Users List** app using what you’ve learned.

### ✅ Output

A list of user names rendered using a reusable component with props and keys.

---

### 📄 Full Example (JSX in HTML using CDN)

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Users List App</title>
    <script src="https://unpkg.com/react@17/umd/react.development.js"></script>
    <script src="https://unpkg.com/react-dom@17/umd/react-dom.development.js"></script>
    <script src="https://unpkg.com/@babel/standalone/babel.min.js"></script>
  </head>
  <body>
    <div id="root"></div>

    <script type="text/babel">
      // Reusable component for each user
      function User(props) {
        return <li>{props.name}</li>;
      }

      // Main component
      function UsersList() {
        const users = ["Alice", "Bob", "Charlie"];

        return (
          <div>
            <h2>User List</h2>
            <ul>
              {users.map((user, index) => (
                <User key={index} name={user} />
              ))}
            </ul>
          </div>
        );
      }

      // Render to DOM
      ReactDOM.render(<UsersList />, document.getElementById("root"));
    </script>
  </body>
</html>
```

---

### ✅ Key Concepts Practiced:

- **Component** (`User`, `UsersList`)
- **Props** (`name`)
- **Keys** (in `.map()`)
- **Composition** (User used inside UsersList)

---

Would you like to:

- Add **more user details** (like email, ID)?
- Add **user input** to let users add names dynamically?
- Move on to **State** and **Events** next?

---

You're doing great! You've built a clean **Users List application** using:

- `App` component to handle the list
- `UserProfile` component to render each user
- Props to pass user data
- Composition to structure your UI

However, you're missing one **important thing** — **React `key` prop** in your `.map()` function. Let me explain and then show you how to fix it.

---

## ❗ Issue: Missing `key` prop

React will show a **warning** in the console:

> "Each child in a list should have a unique 'key' prop."

This is because `UserProfile` is rendered inside a loop, and React needs a `key` to efficiently update the list.

---

## ✅ Fix: Add a `key` prop

Update your `App` component’s `.map()` to include `key={eachItem.uniqueNo}`.

### ✅ Fixed `App.js`:

```jsx
import UserProfile from "./components/UserProfile/index";

const userDetailsList = [
  {
    uniqueNo: 1,
    imageUrl: "https://assets.ccbp.in/frontend/react-js/esther-howard-img.png",
    name: "Esther Howard",
    role: "Software Developer",
  },
  {
    uniqueNo: 2,
    imageUrl: "https://assets.ccbp.in/frontend/react-js/floyd-miles-img.png",
    name: "Floyd Miles",
    role: "Software Developer",
  },
  {
    uniqueNo: 3,
    imageUrl: "https://assets.ccbp.in/frontend/react-js/jacob-jones-img.png",
    name: "Jacob Jones",
    role: "Software Developer",
  },
  {
    uniqueNo: 4,
    imageUrl: "https://assets.ccbp.in/frontend/react-js/esther-devon-lane.png",
    name: "Devon Lane",
    role: "Software Developer",
  },
];

const App = () => (
  <div className="list-container">
    <h1 className="title">Users List</h1>
    <ul>
      {userDetailsList.map((eachItem) => (
        <UserProfile key={eachItem.uniqueNo} userDetails={eachItem} />
      ))}
    </ul>
  </div>
);

export default App;
```

---

## ✅ No Changes Needed in `UserProfile.js`

Your component is clean and working well:

```jsx
const UserProfile = (props) => {
  const { userDetails } = props;
  const { imageUrl, name, role } = userDetails;

  return (
    <li className="user-card-container">
      <img src={imageUrl} className="avatar" alt="avatar" />
      <div className="user-details-container">
        <h1 className="user-name"> {name} </h1>
        <p className="user-designation"> {role} </p>
      </div>
    </li>
  );
};

export default UserProfile;
```

---

## ✅ Summary

| Task                | Status   |
| ------------------- | -------- |
| Reusable Component  | ✅ Done  |
| Props               | ✅ Used  |
| Mapping List        | ✅ Done  |
| Missing Key Warning | ❌ Fixed |
| Composition         | ✅ Good  |

You're ready to move on to **State** and **Event Handling** next if you're up for it — maybe let users **add** or **remove** profiles?

## Want to go there?

Excellent! Let’s take the next big step in learning **React** by covering:

---

## 📚 Topics We’ll Cover:

1. **Components Recap**
2. **Functional Components**
3. **Class Components**
4. **React Events**
5. **State**
6. **Updating State**
7. **State Updates are Merged**
8. **Functional vs Class Components**
9. **Counter Application** Example

---

## 1. 🔁 Components Recap

- **Component** = Reusable piece of UI
- Can be either a **function** or a **class**
- Accept **props** and return JSX

---

## 2. ⚙️ Functional Components

A **Functional Component** is a JavaScript function that returns JSX.

### ✅ Example:

```jsx
function Welcome(props) {
  return <h1>Hello, {props.name}!</h1>;
}
```

You’ve been using these already.

---

## 3. 🏫 Class Components

A **Class Component** uses ES6 class syntax and must extend `React.Component`.

### ✅ Example:

```jsx
import React, { Component } from "react";

class Welcome extends Component {
  render() {
    return <h1>Hello, {this.props.name}!</h1>;
  }
}
```

---

## 4. 🖱️ React Events

React uses **camelCase** for event names and **functions** as event handlers.

### Example: Button click

```jsx
function ClickMe() {
  function handleClick() {
    alert("Button Clicked!");
  }

  return <button onClick={handleClick}>Click Me</button>;
}
```

---

## 5. 📦 State

**State** is data managed inside a component. If state changes, React re-renders the component.

### ✅ Functional Component with `useState`

```jsx
import React, { useState } from "react";

function Counter() {
  const [count, setCount] = useState(0);

  return (
    <div>
      <p>Count: {count}</p>
      <button onClick={() => setCount(count + 1)}>Increase</button>
    </div>
  );
}
```

---

## 6. 🔄 Updating State

Use the setter function returned by `useState`.

```js
setCount(count + 1);
```

> It updates the state and re-renders the component.

---

## 7. ♻️ State Updates are Merged

In **class components**, when you update state with `this.setState()`, React **merges** the new state with the existing one.

### Example:

```jsx
this.setState({ age: 25 });
```

Only `age` gets updated; other state fields remain unchanged.

> In **functional components**, you control the merge manually if using objects.

---

## 8. 🆚 Functional vs Class Components

| Feature              | Functional         | Class                     |
| -------------------- | ------------------ | ------------------------- |
| Syntax               | Function           | Class extends Component   |
| State                | `useState`         | `this.state`              |
| Lifecycle Methods    | `useEffect`        | `componentDidMount`, etc. |
| Simpler Code         | ✅                 | ❌                        |
| Recommended in 2024+ | ✅ (by React team) | ⚠️ Legacy mostly          |

---

## 9. 🧮 Counter Application

Let’s build a simple **Counter App** using a **functional component**.

---

### ✅ Counter App (Functional Component)

```jsx
import React, { useState } from "react";

function Counter() {
  const [count, setCount] = useState(0);

  const increment = () => setCount(count + 1);
  const decrement = () => setCount(count - 1);
  const reset = () => setCount(0);

  return (
    <div style={{ textAlign: "center", marginTop: "50px" }}>
      <h1>Counter: {count}</h1>
      <button onClick={increment}>➕</button>
      <button onClick={decrement}>➖</button>
      <button onClick={reset}>🔁 Reset</button>
    </div>
  );
}

export default Counter;
```

---

### 🧪 You can render it inside `App.js`

```jsx
import Counter from "./Counter";

function App() {
  return (
    <div>
      <h1>Welcome to Counter App</h1>
      <Counter />
    </div>
  );
}
```

---

## Would you like me to also show the **class component version** of the Counter App for comparison?

You're doing everything right! ✅
You've successfully built the **Counter Application using a Class Component** and used `state`, `setState`, and event handlers. Let's break it down and compare it with the functional version you've already seen.

---

## ✅ What You Did Right in Your Code

### 1. **Used a Class Component**

```jsx
class Counter extends Component {
```

### 2. **Defined Initial State**

```jsx
state = { count: 0 };
```

### 3. **Handled Events to Update State**

```jsx
onIncrement = () => {
  this.setState((prevState) => ({ count: prevState.count + 1 }));
};
```

### 4. **Rendered Dynamic State**

```jsx
<h1 className="count">Count {count}</h1>
```

### 5. **Used CSS Class Names**

Good for styling separation:

```jsx
<button className="button" onClick={this.onIncrement}>
```

---

## 🔁 Comparison: Class vs Functional Counter

| Feature           | Class Component                        | Functional Component                    |
| ----------------- | -------------------------------------- | --------------------------------------- |
| Syntax            | `class` + `extends Component`          | `function` + `useState()`               |
| State Declaration | `this.state = { count: 0 }`            | `const [count, setCount] = useState(0)` |
| Update State      | `this.setState()`                      | `setCount()`                            |
| Event Handling    | Arrow functions or bind in constructor | Just define a function                  |
| Simplicity        | More boilerplate                       | Cleaner and shorter                     |
| Recommended       | ❌ Mostly for legacy apps              | ✅ Preferred for new development        |

---

## 🧠 How `setState` Works in Class Components

```js
this.setState((prevState) => ({ count: prevState.count + 1 }));
```

- Ensures the update is **based on the latest state**.
- This is **important** in async scenarios.

---

## ✅ Optional: Add a Reset Button

If you want to expand your app a little:

```jsx
onReset = () => {
  this.setState({ count: 0 });
};
```

```jsx
<button className="button" onClick={this.onReset}>
  Reset
</button>
```

---

## ✅ Summary

| Concept                  | ✅ Done in Your Code |
| ------------------------ | -------------------- |
| Class Component          | ✅                   |
| State with `this.state`  | ✅                   |
| Update with `setState()` | ✅                   |
| React Events             | ✅                   |
| Counter App Logic        | ✅                   |

---

Would you like to:

- Convert this class version into a **functional component** using `useState`?
- Move on to learning about **useEffect** or **conditional rendering**?
- Build a more advanced app like a **To-Do List** or **Theme Switcher**?

Great! Let’s go over **Conditional Rendering** in React step by step, with clear explanations and examples for each method — including **default props** at the end.

---

## 📘 What is Conditional Rendering?

In React, **conditional rendering** means showing UI elements **based on a condition** — just like `if` statements in JavaScript.

---

## ✅ 1. Using an `if...else` Statement

This is good for **more complex logic**.

### Example:

```jsx
function Greeting(props) {
  const isLoggedIn = props.isLoggedIn;

  if (isLoggedIn) {
    return <h1>Welcome back!</h1>;
  } else {
    return <h1>Please log in.</h1>;
  }
}
```

### Usage:

```jsx
<Greeting isLoggedIn={true} />
```

---

## ✅ 2. Using Element Variables

Store JSX in a **variable** and return it conditionally.

### Example:

```jsx
function LoginControl(props) {
  const isLoggedIn = props.isLoggedIn;
  let message;

  if (isLoggedIn) {
    message = <h1>Welcome, user!</h1>;
  } else {
    message = <h1>You need to log in.</h1>;
  }

  return message;
}
```

---

## ✅ 3. Using the Ternary Operator (`condition ? true : false`)

Best for **short inline conditions**.

### Example:

```jsx
function Greeting(props) {
  return <h1>{props.isLoggedIn ? "Welcome Back!" : "Please Sign In"}</h1>;
}
```

---

## ✅ 4. Using Logical `&&` Operator

Useful for rendering **only when a condition is true**.

```jsx
function Notification(props) {
  return <div>{props.hasNewMessages && <p>You have new messages!</p>}</div>;
}
```

If `hasNewMessages` is `false`, React **skips** rendering the `<p>`.

---

## ✅ 5. Default Props

You can set **default values** for props in case the parent component doesn’t pass them.

### Functional Component Default Props:

```jsx
function UserCard({ name = "Guest", age = "N/A" }) {
  return (
    <div>
      <h2>{name}</h2>
      <p>Age: {age}</p>
    </div>
  );
}
```

Or:

```jsx
UserCard.defaultProps = {
  name: "Guest",
  age: "N/A",
};
```

### Usage:

```jsx
<UserCard />  // Renders: Guest, Age: N/A
<UserCard name="Alice" /> // Renders: Alice, Age: N/A
```

---

## 🧪 Bonus Example — Combining Concepts

```jsx
function Dashboard({ username, isLoggedIn }) {
  return (
    <div>
      <h1>{isLoggedIn ? `Welcome, ${username}` : "Please Log In"}</h1>
      {isLoggedIn && <button>Logout</button>}
    </div>
  );
}

Dashboard.defaultProps = {
  username: "Guest",
  isLoggedIn: false,
};
```

---

## ✅ Summary

| Method            | Use Case                    |
| ----------------- | --------------------------- |
| `if...else`       | Complex branches            |
| Element Variables | Store reusable JSX          |
| Ternary Operator  | Simple inline conditions    |
| Logical `&&`      | Render if condition is true |
| Default Props     | Fallback values             |

---

Would you like a small interactive app that **uses all these techniques** (like a login/logout switcher)? Or shall we move on to **Lists and Keys**, **Forms**, or **useEffect** next?

---

You're now entering a really useful part of React — combining **state management**, **input fields**, **callbacks**, and **search functionality**. Let's learn each of these **step by step**, then build a **Searchable Users List App**.

---

## 🔁 1. `setState()` — Object Syntax

In **class components**, the standard `setState` usage is:

```jsx
this.setState({ key: value });
```

Example:

```jsx
this.setState({ count: 10 });
```

👉 It updates only the fields you provide. The rest of the state is preserved.

---

## 📨 2. Sending Function as Callback (After `setState`)

`setState()` is **asynchronous**. If you want to do something **after** the state updates, you can pass a **callback** as the second argument.

### Example:

```jsx
this.setState({ count: this.state.count + 1 }, () => {
  console.log("Count updated:", this.state.count);
});
```

---

## 🔤 3. Input Element in React

React input elements are usually **controlled components**, meaning their value is tied to state.

### Functional Component Input Example:

```jsx
const [searchText, setSearchText] = useState("")

<input
  type="text"
  value={searchText}
  onChange={(e) => setSearchText(e.target.value)}
/>
```

---

## 🔍 4. Searchable Users List Application (Class Component)

### ✅ Final Result Preview:

- Input box for searching
- List filters as you type
- Users displayed with name and role

---

### 🧱 Step-by-Step Full App (Class Component)

#### `App.js`

```jsx
import { Component } from "react";
import UserProfile from "./components/UserProfile";
import "./App.css";

const userDetailsList = [
  {
    uniqueNo: 1,
    imageUrl: "https://assets.ccbp.in/frontend/react-js/esther-howard-img.png",
    name: "Esther Howard",
    role: "Software Developer",
  },
  {
    uniqueNo: 2,
    imageUrl: "https://assets.ccbp.in/frontend/react-js/floyd-miles-img.png",
    name: "Floyd Miles",
    role: "Software Developer",
  },
  {
    uniqueNo: 3,
    imageUrl: "https://assets.ccbp.in/frontend/react-js/jacob-jones-img.png",
    name: "Jacob Jones",
    role: "Software Developer",
  },
  {
    uniqueNo: 4,
    imageUrl: "https://assets.ccbp.in/frontend/react-js/esther-devon-lane.png",
    name: "Devon Lane",
    role: "Software Developer",
  },
];

class App extends Component {
  state = {
    searchInput: "",
  };

  onChangeSearchInput = (event) => {
    this.setState({ searchInput: event.target.value });
  };

  render() {
    const { searchInput } = this.state;
    const filteredList = userDetailsList.filter((user) =>
      user.name.toLowerCase().includes(searchInput.toLowerCase())
    );

    return (
      <div className="list-container">
        <h1 className="title">Users List</h1>
        <input
          type="search"
          placeholder="Search by name"
          value={searchInput}
          onChange={this.onChangeSearchInput}
          className="search-input"
        />
        <ul>
          {filteredList.map((eachItem) => (
            <UserProfile key={eachItem.uniqueNo} userDetails={eachItem} />
          ))}
        </ul>
      </div>
    );
  }
}

export default App;
```

---

#### `UserProfile.js`

```jsx
import "./index.css";

const UserProfile = (props) => {
  const { userDetails } = props;
  const { imageUrl, name, role } = userDetails;

  return (
    <li className="user-card-container">
      <img src={imageUrl} className="avatar" alt={name} />
      <div className="user-details-container">
        <h1 className="user-name">{name}</h1>
        <p className="user-designation">{role}</p>
      </div>
    </li>
  );
};

export default UserProfile;
```

---

## ✅ Summary

| Concept                    | Used In App |
| -------------------------- | ----------- |
| `setState({})`             | ✅          |
| Callback after `setState`  | Optional    |
| Controlled Input Element   | ✅          |
| Filtering with `.filter()` | ✅          |
| Conditional Rendering      | ✅          |

---

## Would you like the **functional component** version of this app? Or should we add **delete functionality**, **form submission**, or **styling next**?

Perfect! Let’s convert the **Searchable Users List Application** into a **Functional Component version** using `useState`.

---

## ✅ Functional Component Version of the App

We’ll use the same `userDetailsList`, and handle:

- State with `useState`
- Input change with `onChange`
- Filtering with `.filter()`

---

### `App.js`

```jsx
import { useState } from "react";
import UserProfile from "./components/UserProfile";
import "./App.css";

const userDetailsList = [
  {
    uniqueNo: 1,
    imageUrl: "https://assets.ccbp.in/frontend/react-js/esther-howard-img.png",
    name: "Esther Howard",
    role: "Software Developer",
  },
  {
    uniqueNo: 2,
    imageUrl: "https://assets.ccbp.in/frontend/react-js/floyd-miles-img.png",
    name: "Floyd Miles",
    role: "Software Developer",
  },
  {
    uniqueNo: 3,
    imageUrl: "https://assets.ccbp.in/frontend/react-js/jacob-jones-img.png",
    name: "Jacob Jones",
    role: "Software Developer",
  },
  {
    uniqueNo: 4,
    imageUrl: "https://assets.ccbp.in/frontend/react-js/esther-devon-lane.png",
    name: "Devon Lane",
    role: "Software Developer",
  },
];

const App = () => {
  const [searchInput, setSearchInput] = useState("");

  const onChangeSearchInput = (event) => {
    setSearchInput(event.target.value);
  };

  const filteredList = userDetailsList.filter((user) =>
    user.name.toLowerCase().includes(searchInput.toLowerCase())
  );

  return (
    <div className="list-container">
      <h1 className="title">Users List</h1>
      <input
        type="search"
        placeholder="Search by name"
        value={searchInput}
        onChange={onChangeSearchInput}
        className="search-input"
      />
      <ul>
        {filteredList.map((user) => (
          <UserProfile key={user.uniqueNo} userDetails={user} />
        ))}
      </ul>
    </div>
  );
};

export default App;
```

---

### `UserProfile.js`

No change is needed from the previous version, but here’s the full code again for clarity:

```jsx
import "./index.css";

const UserProfile = (props) => {
  const { userDetails } = props;
  const { imageUrl, name, role } = userDetails;

  return (
    <li className="user-card-container">
      <img src={imageUrl} className="avatar" alt={name} />
      <div className="user-details-container">
        <h1 className="user-name">{name}</h1>
        <p className="user-designation">{role}</p>
      </div>
    </li>
  );
};

export default UserProfile;
```

---

## ✅ Summary of Functional Version

| Feature        | Code Used                 |
| -------------- | ------------------------- |
| State          | `useState`                |
| Event Handling | `onChange` with arrow fn  |
| Filtering Data | `.filter()` inside render |
| Reusability    | Functional `UserProfile`  |

---

Let me know if you want to:

- Add **delete** or **edit** functionality,
- Convert this to **TypeScript**,
- Add **form validation**, or
- Use **Context API** for global state.

---

Great list! These are **common mistakes** many beginners (and even experienced devs) make when working with **React** — especially when transitioning between vanilla JavaScript, JSX, and class/functional components.

Let’s go through each one with **clear explanations and correct examples**.

---

## 🔴 1. **Missing Export Statement**

**Mistake:**

```js
const App = () => { ... }
// Forgot to export
```

✅ **Fix:**

```js
export default App;
```

---

## 🔴 2. **Missing Import Statement**

**Mistake:**

```js
// Using useState without importing it
const [value, setValue] = useState("");
```

✅ **Fix:**

```js
import React, { useState } from "react";
```

---

## 🔴 3. **Missing `extends React.Component`**

**Mistake:**

```js
class MyComponent {
  render() {
    return <h1>Hello</h1>;
  }
}
```

✅ **Fix:**

```js
import React, { Component } from "react";

class MyComponent extends Component {
  render() {
    return <h1>Hello</h1>;
  }
}
```

---

## 🔴 4. `class` vs `className`

**Mistake:**

```jsx
<div class="header">Welcome</div>
```

✅ **Fix:**

```jsx
<div className="header">Welcome</div>
```

📝 JSX uses `className` instead of `class` because `class` is a reserved keyword in JavaScript.

---

## 🔴 5. `onclick` vs `onClick`

**Mistake:**

```jsx
<button onclick={handleClick}>Click</button>
```

✅ **Fix:**

```jsx
<button onClick={handleClick}>Click</button>
```

📝 React uses **camelCase** for event handlers.

---

## 🔴 6. Event Listeners inside Class Component

**Mistake:**
Not using `this` or forgetting arrow functions:

```js
<button onClick={handleClick}>Click</button> // handleClick not defined
```

✅ **Fix:**

```jsx
<button onClick={this.handleClick}>Click</button>
```

And either bind it in constructor:

```js
this.handleClick = this.handleClick.bind(this);
```

or use arrow function:

```js
handleClick = () => { ... }
```

---

## 🔴 7. Passing Event Handler (Don't Invoke It!)

**Mistake:**

```jsx
<button onClick={this.handleClick()}>Click</button> // ❌ Invoked immediately
```

✅ **Fix:**

```jsx
<button onClick={this.handleClick}>Click</button>
```

✅ Or pass arguments safely:

```jsx
<button onClick={() => this.handleClick(arg)}>Click</button>
```

---

## 🔴 8. Modifying State Directly

**Mistake:**

```js
this.state.count = 10; // ❌ will not re-render
```

✅ **Fix:**

```js
this.setState({ count: 10 });
```

---

## 🔴 9. Calling `setState()` from `render()`

**Mistake:**

```js
render() {
  this.setState({ count: 5 }) // ❌ Infinite loop!
  return <h1>Hi</h1>
}
```

✅ **Fix:**
Never call `setState` in `render()`. Use `componentDidMount` or event handlers.

---

## 🔴 10. Invoking Event Handler Directly

Same as #7 — Don’t do this:

```jsx
onClick={handleClick()} // ❌ Immediately runs
```

✅ Do this:

```jsx
onClick = { handleClick }; // ✅ Reference only
```

---

## 🔴 11. `setState()` is Asynchronous

**Mistake:**

```js
this.setState({ count: this.state.count + 1 });
console.log(this.state.count); // ❌ Not updated yet
```

✅ **Fix:**
Use callback or functional form:

```js
this.setState((prevState) => ({ count: prevState.count + 1 }));
```

---

## 🔴 12. Component must return **one JSX element**

**Mistake:**

```jsx
return (
  <h1>Hello</h1>
  <p>World</p>
) // ❌ Error
```

✅ **Fix:**
Wrap with a single parent element or Fragment:

```jsx
return (
  <div>
    <h1>Hello</h1>
    <p>World</p>
  </div>
);

// OR use Fragment
return (
  <>
    <h1>Hello</h1>
    <p>World</p>
  </>
);
```

---

## 🔴 13. Using `props` as mutable (Read-Only Violation)

**Mistake:**

```js
props.name = "John"; // ❌ Not allowed
```

✅ **Fix:**
Props are **read-only**. If you need to change something, use state.

---

## ✅ Summary Table

| Mistake                           | Fix                                        |
| --------------------------------- | ------------------------------------------ |
| Missing export/import             | Use `export default` and `import` properly |
| `class` vs `className`            | Use `className` in JSX                     |
| `onclick` vs `onClick`            | React uses camelCase                       |
| Event handlers in class           | Use `this` or arrow functions              |
| Calling handlers directly         | Use `onClick={handler}` not `handler()`    |
| Direct state mutation             | Always use `setState()`                    |
| Calling `setState` in `render()`  | Never do it inside `render()`              |
| `setState` async                  | Use callback or functional form            |
| Component must return one element | Use `<div>` or `<>` Fragments              |
| Props are read-only               | Don’t assign to `props`                    |

---

Would you like practice problems or interactive code tasks for any of these mistakes?

---

You're absolutely right — **debugging** is a critical skill in React development (and in all programming). Let's expand on your explanation with **clear structure, tools, and examples**, so you understand **how and when to use each debugging technique** effectively.

---

## 🐞 Debugging in React

> **Debugging** = The process of **finding** and **fixing bugs** in your code.

In React, bugs often come from:

- Incorrect state or props
- Rendering issues
- Event handler mistakes
- Logic or data flow problems

---

## 🛠️ 1. **Browser Developer Tools**

All modern browsers (like Chrome, Firefox, Edge) provide built-in **developer tools**.

### 📋 What You Can Do:

| Feature             | Description                             |
| ------------------- | --------------------------------------- |
| **Elements tab**    | View/edit live HTML & CSS               |
| **Console tab**     | See `console.log`, errors, and warnings |
| **Network tab**     | Monitor API requests/responses          |
| **Sources tab**     | Add breakpoints in JavaScript           |
| **Responsive mode** | Test different screen sizes             |

### ✅ Use Cases:

- See if your component is rendering correctly
- Verify styles or className issues
- Check if an API call worked
- Log values (`console.log(state)`)

---

## 🧩 2. **React Developer Tools**

> A browser extension built specifically for debugging React applications.

### 🔧 Install:

- Chrome: [React Developer Tools on Chrome Web Store](https://chrome.google.com/webstore/detail/react-developer-tools/fmkadmapgofadopljbjfkapdkoienihi)

### 📋 What You Can Do:

| Feature               | Description                                                  |
| --------------------- | ------------------------------------------------------------ |
| **Component Tree**    | View hierarchy of components (App → Header → ListItem, etc.) |
| **Props**             | See what props are passed to each component                  |
| **State**             | View and modify component state in real-time                 |
| **Hooks**             | See `useState`, `useEffect`, etc.                            |
| **Highlight updates** | Detect which components re-render on state change            |

### ✅ Use Cases:

- Check if your component received the correct props
- See live state updates in functional components
- Diagnose unnecessary re-renders

---

## 🧪 Example Debug Flow

Let’s say a button is supposed to increase a counter, but it’s not working.

### Debugging Steps:

1. **Use `console.log` in the event handler**
   → Did the function run?

2. **Open React Developer Tools**
   → Is the state (`count`) updating?

3. **Use Browser Dev Tools → Elements**
   → Is the button visible, and is `onClick` properly assigned?

4. **Use Dev Tools → Console**
   → Are there any warnings or errors?

---

## 🔥 Tips for Better Debugging

✅ Always use meaningful `console.log()`:

```js
console.log("Button clicked", count);
```

✅ Use `debugger;` to pause code execution in DevTools.

✅ Use try/catch blocks for catching runtime errors:

```js
try {
  riskyFunction();
} catch (error) {
  console.error("Something went wrong:", error);
}
```

✅ Don’t ignore warnings! React gives useful hints like:

```
Warning: Each child in a list should have a unique "key" prop.
```

---

## 📦 Additional Tools

| Tool                                      | Purpose                             |
| ----------------------------------------- | ----------------------------------- |
| **Linting (ESLint)**                      | Catch common mistakes early         |
| **Type Checking (TypeScript/PropTypes)**  | Detect type-related bugs            |
| **Testing (Jest, React Testing Library)** | Ensure components work as expected  |
| **Redux DevTools**                        | Debug global state when using Redux |

---

## ✅ Summary

| Tool                  | Best For                            |
| --------------------- | ----------------------------------- |
| **Console.log()**     | Quick debugging                     |
| **Browser Dev Tools** | Styling, layout, JS errors          |
| **React Dev Tools**   | State, props, hooks, component tree |
| **Network Tab**       | API requests                        |
| **Breakpoints**       | Step-by-step debugging              |

---

Would you like a **hands-on debugging example**, or want help with debugging a real problem you're facing in your React project?
