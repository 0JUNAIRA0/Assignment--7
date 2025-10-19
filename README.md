# 🧠 React Fundamentals — Q&A
---

## ⚙️ What is JSX, and Why is it Used?

**JSX (JavaScript XML)** is a syntax extension for JavaScript used in React to describe the UI.  
It allows developers to write HTML-like code directly inside JavaScript files, making the code more readable and expressive.

Example:
```jsx
const element = <h1>Hello, React!</h1>;
```

JSX gets compiled into regular JavaScript using tools like **Babel**, and React then uses it to create virtual DOM elements.

✅ **Benefits:**
- Makes code more readable and expressive  
- Integrates HTML structure with JavaScript logic  
- Enables easier component-based UI building  

---

## 🔄 What is the Difference Between State and Props?

| Feature | **State** | **Props** |
|----------|------------|-----------|
| Definition | Internal data of a component | Data passed from parent to child component |
| Mutability | Mutable (can be changed using `setState` or hooks like `useState`) | Immutable (cannot be modified by the child) |
| Managed by | Component itself | Parent component |
| Usage | Used for dynamic data that changes over time | Used to pass data and functions between components |

**Example:**
```jsx
// State example
const [count, setCount] = useState(0);

// Props example
<MyButton title="Click Me" />
```

---

## ⚡ What is the useState Hook, and How Does It Work?

`useState` is a **React Hook** that allows you to add and manage state in a functional component.

**Syntax:**
```jsx
const [value, setValue] = useState(initialValue);
```

**How it works:**
1. It declares a state variable (`value`) and a setter function (`setValue`).
2. When `setValue` is called, React re-renders the component with the updated state.

**Example:**
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

## 🤝 How Can You Share State Between Components in React?

I can share state between components using these approaches:

1. **Lifting State Up** – Move the state to a common parent component and pass it down as props.
2. **React Context API** – Useful for global state accessible by many components.
3. **State Management Libraries** – Use tools like Redux, Zustand, or Recoil for complex applications.

**Example (Lifting State Up):**
```jsx
function Parent() {
  const [message, setMessage] = useState("Hello!");

  return <Child message={message} />;
}

function Child({ message }) {
  return <p>{message}</p>;
}
```

---

## 🖱️ How is Event Handling Done in React?

Event handling in React is similar to handling events in JavaScript, but with **camelCase syntax** and passing **functions** instead of strings.

**Example:**
```jsx
function Button() {
  const handleClick = () => {
    alert("Button clicked!");
  };

  return <button onClick={handleClick}>Click Me</button>;
}
```



---

**© 2025 React Learning Guide — All Rights Reserved.**
