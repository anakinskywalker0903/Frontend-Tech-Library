# Barba.js

> A small JavaScript library for creating smooth and seamless transitions between webpages.

## 🔗 Links

* **Website:** https://barba.js.org/
* **Documentation:** https://barba.js.org/docs/
* **GitHub:** https://github.com/barbajs/barba

## 📌 What is Barba.js?

Barba.js is a JavaScript library that helps create smooth transitions between pages by preventing full browser reloads and managing page transitions.

It can make traditional multi-page websites feel more like modern single-page applications.

## ✨ What can you build?

* Page transition animations
* Smooth navigation experiences
* Loading transitions
* Enter/leave page animations
* SPA-like navigation on traditional websites

## 🧠 Key Concepts

* **Transitions** — Define animations when leaving and entering pages.
* **Views** — Add page-specific behavior.
* **Hooks** — Run code at different points during navigation.
* **Containers** — Define the part of the page that Barba replaces.

## ⚙️ Installation

```bash
npm install @barba/core
```

## 🧪 Basic Example

```javascript
import barba from '@barba/core';

barba.init({
  transitions: [
    {
      name: 'default-transition',

      leave() {
        // Leave animation
      },

      enter() {
        // Enter animation
      }
    }
  ]
});
```

## 🎯 Best Used For

Websites where page transitions and motion are an important part of the user experience, especially portfolios, creative websites, agency websites, and highly interactive sites.

## ⚠️ Keep in Mind

Barba.js is primarily focused on **page transitions and navigation**, not on building UI components or replacing a frontend framework.

It can also be combined with animation libraries such as **GSAP** for more advanced transitions.

## 📚 Useful Resources

* Official Documentation: https://barba.js.org/docs/
* GitHub: https://github.com/barbajs/barba
* Examples: https://barba.js.org/docs/getstarted/basic-usage/
