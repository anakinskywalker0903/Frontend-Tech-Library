# Preact

> A fast, lightweight alternative to React with a similar modern component-based API.

## 🔗 Links

* **Website:** https://preactjs.com/
* **Documentation:** https://preactjs.com/guide/
* **GitHub:** https://github.com/preactjs/preact

## 📌 What is Preact?

Preact is a lightweight JavaScript library for building user interfaces using a component-based architecture similar to React.

It provides much of the React development experience while keeping the library itself extremely small.

## ✨ Key Features

* Lightweight bundle size
* React-like API
* Component-based development
* JSX support
* Hooks
* Fast rendering
* React compatibility through `preact/compat`

## ⚙️ Installation

```bash
npm install preact
```

## 🧪 Basic Example

```jsx
import { render } from 'preact';

function App() {
  return <h1>Hello Preact!</h1>;
}

render(<App />, document.getElementById('app'));
```

## 🧠 React Compatibility

Preact provides a compatibility layer that allows many React libraries and applications to work with Preact.

```javascript
import React from 'preact/compat';
```

This is especially useful when you want to use the React ecosystem while keeping the runtime lightweight.

## 🎯 Best Used For

* Lightweight web applications
* Performance-focused websites
* PWAs
* Interactive websites
* Projects where bundle size matters
* Embedded widgets and components

## ⚠️ Keep in Mind

Preact is **not simply a smaller version of React**. Although its API is intentionally similar, there can be differences in behavior and ecosystem compatibility.

Check library compatibility before replacing React with Preact in an existing project.

## 📚 Useful Resources

* Official Guide: https://preactjs.com/guide/
* API Reference: https://preactjs.com/guide/v10/api-reference/
* React Compatibility: https://preactjs.com/guide/v10/switching-to-preact/
* GitHub: https://github.com/preactjs/preact
