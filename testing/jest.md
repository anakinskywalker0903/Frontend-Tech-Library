# Jest

> A JavaScript testing framework designed for testing JavaScript and TypeScript code.

## 🔗 Links

* **Website:** https://jestjs.io/
* **Documentation:** https://jestjs.io/docs/getting-started
* **GitHub:** https://github.com/jestjs/jest

## 📌 What is Jest?

Jest is a JavaScript testing framework developed by Meta. It provides tools for writing, running, and evaluating automated tests.

It is commonly used for testing JavaScript and TypeScript applications, including React projects.

## ✨ Key Features

* Unit testing
* Snapshot testing
* Mocking
* Code coverage
* Assertions
* Fast test execution
* Built-in test runner

## ⚙️ Installation

```bash
npm install --save-dev jest
```

## 🧪 Basic Example

```javascript
function add(a, b) {
  return a + b;
}

test('adds two numbers', () => {
  expect(add(2, 3)).toBe(5);
});
```

## 🧠 Common Methods

```javascript
expect(value).toBe(expected);
expect(value).toEqual(expected);

test('example', () => {
  // test
});
```

## 🎯 Best Used For

* Testing JavaScript functions
* Unit testing
* Testing React applications
* Testing business logic
* Regression testing

## ⚠️ Keep in Mind

Jest is primarily a **testing framework**, not a frontend framework or UI library.

For modern frontend projects, it can be used alongside tools such as React Testing Library.

## 📚 Useful Resources

* Official Documentation: https://jestjs.io/docs/getting-started
* API Reference: https://jestjs.io/docs/api
* GitHub: https://github.com/jestjs/jest
