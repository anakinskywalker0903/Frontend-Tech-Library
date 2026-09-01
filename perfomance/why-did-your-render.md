# why-did-you-render (WDYR)

> A debugging tool that helps identify unnecessary re-renders in React applications.

## 🔗 Links

* **GitHub:** https://github.com/welldone-software/why-did-you-render
* **Documentation:** https://github.com/welldone-software/why-did-you-render

## 📌 What is why-did-you-render?

**why-did-you-render (WDYR)** is a React debugging tool that tracks component re-renders and reports when a component re-renders unnecessarily.

It is particularly useful when investigating performance problems caused by excessive rendering.

## ✨ Key Features

* Detects unnecessary re-renders
* Tracks React component updates
* Shows why a component rendered
* Helps identify changing props
* Helps detect avoidable state updates
* Useful for React performance debugging

## 🧠 Why Re-renders Matter

React components can re-render when their state, props, or other dependencies change.

Some re-renders are necessary, while others can happen because of things such as:

* New object references
* New function references
* Unnecessary state updates
* Changing props
* Parent component re-renders

WDYR helps identify these situations.

## ⚙️ Installation

```bash id="q8m4zs"
npm install @welldone-software/why-did-you-render --save-dev
```

## 🧪 Basic Setup

Create a separate configuration file, for example:

```javascript id="p5v7kn"
import React from "react";

if (process.env.NODE_ENV === "development") {
  const whyDidYouRender = require("@welldone-software/why-did-you-render");

  whyDidYouRender(React, {
    trackAllPureComponents: true,
  });
}
```

## 🔍 Example

WDYR can report information such as:

```text id="r2x6wp"
Component re-rendered

Reason:
Props changed

Previous:
{ user: {...} }

Next:
{ user: {...} }
```

This can help reveal cases where two objects contain the same data but have different references.

## 🎯 Best Used For

* React performance debugging
* Finding unnecessary re-renders
* Optimizing large React applications
* Investigating slow components
* Understanding component rendering behavior

## ⚠️ Keep in Mind

WDYR is a **development/debugging tool**, not something you normally need in production.

It also shouldn't be used as the first solution to every performance issue. React DevTools Profiler and proper performance measurement should be used alongside it.

## 📚 Useful Resources

* GitHub: https://github.com/welldone-software/why-did-you-render
* React DevTools: https://react.dev/learn/react-developer-tools
