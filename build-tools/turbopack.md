# Turbopack

> An incremental bundler optimized for JavaScript and TypeScript applications, built in Rust.

## 🔗 Links

* **Website:** https://turbo.build/pack
* **Documentation:** https://nextjs.org/docs/architecture/turbopack
* **GitHub:** https://github.com/vercel/turborepo/tree/main/crates/turborepo-lib

## 📌 What is Turbopack?

Turbopack is a high-performance JavaScript and TypeScript bundler developed by Vercel.

It is designed to provide fast development builds and incremental compilation, particularly for large applications.

Turbopack is deeply integrated with the **Next.js** ecosystem.

## ✨ Key Features

* Built with Rust
* Incremental computation
* Fast development builds
* JavaScript and TypeScript support
* Designed for large codebases
* Integrated with Next.js
* Fast Hot Module Replacement (HMR)

## 🧠 Key Concept

Turbopack uses **incremental computation** to avoid rebuilding work that has not changed.

Instead of repeatedly processing an entire application, it can reuse previous computation results and update only what is necessary.

## ⚙️ Usage with Next.js

Modern Next.js projects can use Turbopack during development:

```bash id="g3yd1f"
next dev --turbopack
```

Depending on the Next.js version, Turbopack may also be enabled through the project's scripts or configuration.

## 🎯 Best Used For

* Next.js applications
* Large JavaScript/TypeScript projects
* Fast local development
* Projects that benefit from incremental builds

## ⚠️ Keep in Mind

Turbopack is primarily a **bundler/build tool**, not a framework.

Its feature support and behavior can vary depending on the version of Next.js and the specific project setup.

## 📚 Useful Resources

* Turbopack: https://turbo.build/pack
* Next.js Turbopack Docs: https://nextjs.org/docs/architecture/turbopack
* Turbopack GitHub: https://github.com/vercel/turborepo/tree/main/crates/turborepo-lib
