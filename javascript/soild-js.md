# SolidJS

> A declarative JavaScript framework for building fast, reactive user interfaces.

## 🔗 Links

* **Website:** https://www.solidjs.com/
* **Documentation:** https://docs.solidjs.com/
* **GitHub:** https://github.com/solidjs/solid

## 📌 What is SolidJS?

SolidJS is a JavaScript framework for building reactive user interfaces.

It uses a fine-grained reactivity system, meaning updates can target only the specific parts of the UI that need to change instead of re-rendering entire components.

Its syntax is similar to React and uses JSX, but its rendering and reactivity model are fundamentally different.

## ✨ Key Features

* Fine-grained reactivity
* JSX support
* Reactive primitives
* High performance
* Small runtime
* No Virtual DOM
* Component-based architecture
* TypeScript support

## 🧠 Key Concept

SolidJS tracks exactly which pieces of state are used by which parts of the UI.

When a value changes, Solid updates only the affected DOM nodes.

```text id="q9r2mt"
State changes
     ↓
Solid tracks dependencies
     ↓
Only affected DOM updates
```

## ⚙️ Create a Project

```bash id="j8d4xk"
npm create solid@latest
```

## 🧪 Basic Example

```jsx id="q2b5tz"
import { createSignal } from "solid-js";

function Counter() {
  const [count, setCount] = createSignal(0);

  return (
    <button onClick={() => setCount(count() + 1)}>
      Count: {count()}
    </button>
  );
}

export default Counter;
```

## 🧠 Common Concepts

* **Signals** — Reactive state values.
* **Effects** — Run code when reactive dependencies change.
* **Memos** — Create derived reactive values.
* **Stores** — Manage more complex reactive state.
* **Components** — Reusable UI building blocks.

## 🎯 Best Used For

* Interactive web applications
* Performance-focused interfaces
* Reactive dashboards
* SPAs
* Modern frontend projects
* Projects where fine-grained reactivity is useful

## ⚠️ Keep in Mind

SolidJS has a React-like syntax but **does not use React's rendering model**.

Concepts such as hooks, state, and component rendering work differently, so React knowledge does not translate directly to every SolidJS pattern.

## 📚 Useful Resources

* Documentation: https://docs.solidjs.com/
* Solid Start: https://start.solidjs.com/
* GitHub: https://github.com/solidjs/solid
* Examples: https://www.solidjs.com/examples
