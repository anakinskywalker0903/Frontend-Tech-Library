# Husky

> A tool for managing Git hooks in JavaScript and Node.js projects.

## 🔗 Links

* **Website:** https://typicode.github.io/husky/
* **Documentation:** https://typicode.github.io/husky/
* **GitHub:** https://github.com/typicode/husky

## 📌 What is Husky?

Husky makes it easy to use **Git hooks** in a project.

Git hooks allow you to automatically run scripts at specific points in the Git workflow, such as before a commit or before pushing code.

This is useful for automatically checking code quality and preventing bad code from being committed.

## ✨ Key Features

* Git hook management
* Pre-commit checks
* Pre-push checks
* Works with JavaScript/Node.js projects
* Easy integration with linting and testing tools
* Helps enforce project standards

## 🧠 What are Git Hooks?

Git hooks are scripts that Git runs automatically when certain events occur.

Common hooks include:

```text id="4n1w0a"
pre-commit
pre-push
commit-msg
post-merge
```

For example:

```text id="v9m3kg"
git commit
    ↓
pre-commit hook
    ↓
Run lint/tests
    ↓
Commit created
```

## ⚙️ Installation

```bash id="1h8vqp"
npm install --save-dev husky
```

Initialize Husky:

```bash id="x5j9kc"
npx husky init
```

This sets up Husky and creates a `pre-commit` hook.

## 🧪 Example

A pre-commit hook can run your tests or linter before allowing a commit:

```bash id="j2k7ps"
npm test
```

You can also combine Husky with tools such as:

* ESLint
* Prettier
* Jest
* lint-staged

## 🎯 Best Used For

* Enforcing code quality
* Running tests before commits
* Running linters automatically
* Preventing accidental bad commits
* Standardizing team Git workflows

## ⚠️ Keep in Mind

Husky manages **Git hooks**; it does not replace your testing, linting, or formatting tools.

It is most useful when combined with tools such as ESLint, Prettier, Jest, or lint-staged.

## 📚 Useful Resources

* Documentation: https://typicode.github.io/husky/
* GitHub: https://github.com/typicode/husky
* Git Hooks Documentation: https://git-scm.com/docs/githooks
