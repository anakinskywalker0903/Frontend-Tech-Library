# Cypress

> A JavaScript-based testing framework for testing web applications directly in the browser.

## 🔗 Links

* **Website:** https://www.cypress.io/
* **Documentation:** https://docs.cypress.io/
* **GitHub:** https://github.com/cypress-io/cypress

## 📌 What is Cypress?

Cypress is a testing framework designed for modern web applications.

It runs tests in a real browser environment, allowing developers to test how an application behaves from the perspective of a user.

Cypress is commonly used for **end-to-end (E2E)** and **component testing**.

## ✨ Key Features

* End-to-end testing
* Component testing
* Browser-based test runner
* Automatic waiting
* Time-travel debugging
* Screenshots and videos
* Network request stubbing
* Interactive test runner

## 🧠 How It Works

Unlike traditional testing tools that run outside the browser and communicate with it remotely, Cypress runs closely alongside the application inside the browser environment.

```text id="g7k3qm"
Test
 ↓
Cypress
 ↓
Browser
 ↓
Web Application
```

## ⚙️ Installation

```bash id="x8v2ld"
npm install cypress --save-dev
```

Open Cypress:

```bash id="w4k6pz"
npx cypress open
```

Run tests from the command line:

```bash id="t2r9nf"
npx cypress run
```

## 🧪 Basic Example

```javascript id="m5q1sk"
describe("Login", () => {
  it("allows a user to log in", () => {
    cy.visit("/login");

    cy.get("#email").type("user@example.com");
    cy.get("#password").type("password");

    cy.get("button").click();

    cy.url().should("include", "/dashboard");
  });
});
```

## 🧩 Common Commands

```javascript id="c8v4za"
cy.visit("/");

cy.get("button");

cy.click();

cy.type("Hello");

cy.contains("Welcome");

cy.url();

cy.intercept();
```

## 🎯 Best Used For

* End-to-end testing
* Testing user flows
* Login and authentication flows
* Form testing
* Component testing
* Regression testing
* Testing frontend applications

## ⚠️ Keep in Mind

Cypress is primarily focused on **web application testing**.

It is different from Jest: Jest is commonly used for unit and logic testing, while Cypress is particularly useful for testing application behavior and complete user flows in a browser.

## 📚 Useful Resources

* Documentation: https://docs.cypress.io/
* Guides: https://docs.cypress.io/app/get-started/why-cypress
* Examples: https://example.cypress.io/
* GitHub: https://github.com/cypress-io/cypress
