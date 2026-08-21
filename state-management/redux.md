# Redux

> A predictable state management library for JavaScript applications.

## 🔗 Links

* **Website:** https://redux.js.org/
* **Documentation:** https://redux.js.org/introduction/getting-started
* **GitHub:** https://github.com/reduxjs/redux

## 📌 What is Redux?

Redux is a state management library used to manage and update application state in a predictable way.

It stores application state in a centralized **store** and updates that state through well-defined actions and reducers.

Redux is commonly used with React through **React-Redux**.

## 🧠 Core Concepts

### Store

The central location that holds the application's state.

### Action

An object describing what happened.

```javascript
{
  type: "counter/increment"
}
```

### Reducer

A function that determines how the state changes in response to an action.

### Dispatch

The mechanism used to send an action to the Redux store.

```javascript
dispatch({ type: "counter/increment" });
```

### Selector

A function used to read specific data from the Redux state.

## 🔄 Data Flow

```text
UI
 ↓
Dispatch Action
 ↓
Redux Store
 ↓
Reducer
 ↓
Updated State
 ↓
UI
```

## ⚙️ Installation

For modern Redux applications, use **Redux Toolkit**:

```bash
npm install @reduxjs/toolkit react-redux
```

## 🧪 Basic Example

```javascript
import { createSlice } from "@reduxjs/toolkit";

const counterSlice = createSlice({
  name: "counter",

  initialState: {
    value: 0,
  },

  reducers: {
    increment: (state) => {
      state.value += 1;
    },
  },
});

export const { increment } = counterSlice.actions;
export default counterSlice.reducer;
```

## 🚀 Redux Toolkit

**Redux Toolkit (RTK)** is the recommended way to write Redux logic.

It simplifies common Redux patterns and provides utilities such as:

* `configureStore`
* `createSlice`
* `createAsyncThunk`
* RTK Query

## 🎯 Best Used For

* Large React applications
* Complex shared state
* Applications with predictable state transitions
* State that needs to be accessed across many components
* Applications requiring structured state management

## ⚠️ Keep in Mind

Redux is not necessary for every React application.

For smaller applications, React's built-in state management tools such as `useState` and `useContext` may be sufficient.

For modern Redux projects, prefer **Redux Toolkit** rather than writing traditional Redux boilerplate manually.

## 📚 Useful Resources

* Redux Documentation: https://redux.js.org/
* Redux Toolkit: https://redux-toolkit.js.org/
* React Redux: https://react-redux.js.org/
* Redux GitHub: https://github.com/reduxjs/redux
