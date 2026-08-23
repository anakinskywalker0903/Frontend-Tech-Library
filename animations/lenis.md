# Lenis

> A lightweight smooth scrolling library for creating smooth and customizable scroll experiences on the web.

## 🔗 Links

* **Website:** https://lenis.darkroom.engineering/
* **Documentation:** https://github.com/darkroomengineering/lenis
* **GitHub:** https://github.com/darkroomengineering/lenis

## 📌 What is Lenis?

Lenis is a lightweight JavaScript library that provides smooth, customizable scrolling for websites.

It gives developers more control over scrolling behavior and can be combined with animation libraries such as GSAP and Motion to create advanced scroll-based experiences.

## ✨ Key Features

* Smooth scrolling
* Lightweight
* Customizable scroll behavior
* Touch and wheel support
* Scroll event APIs
* Works with animation libraries
* Designed for modern websites

## 🧠 Key Concept

Lenis sits between the user's input and the website's scrolling behavior.

```text id="c6p2wj"
User Scroll
     ↓
   Lenis
     ↓
Smooth Scroll
     ↓
Scroll-based Animations
```

## ⚙️ Installation

```bash id="v4m9qs"
npm install lenis
```

## 🧪 Basic Example

```javascript id="x2r7km"
import Lenis from "lenis";

const lenis = new Lenis();

function raf(time) {
  lenis.raf(time);
  requestAnimationFrame(raf);
}

requestAnimationFrame(raf);
```

## 🔗 Using with GSAP

Lenis can be combined with GSAP's animation system to build more advanced scroll experiences.

```text id="b8q5nd"
Lenis
  ↓
Smooth scrolling
  ↓
Scroll position
  ↓
GSAP ScrollTrigger
  ↓
Scroll animations
```

## 🎯 Best Used For

* Portfolio websites
* Creative websites
* Agency websites
* Smooth scrolling experiences
* Scroll-based animations
* Interactive landing pages

## ⚠️ Keep in Mind

Lenis changes the scrolling behavior of a website, so it should be used carefully.

Avoid adding smooth scrolling simply because it looks impressive. Accessibility, touch behavior, performance, and the overall UX should still be considered.

## 📚 Useful Resources

* Documentation: https://github.com/darkroomengineering/lenis
* GitHub: https://github.com/darkroomengineering/lenis
* Examples: https://lenis.darkroom.engineering/
