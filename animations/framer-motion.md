# Framer Motion

> A React animation library for creating smooth, production-ready animations and interactions.

## 🔗 Links

* **Website:** https://motion.dev/
* **Documentation:** https://motion.dev/docs
* **GitHub:** https://github.com/motiondivision/motion

## 📌 What is Framer Motion?

Framer Motion is a React animation library that makes it easier to add animations, transitions, gestures, and interactive motion to React applications.

It is now part of the **Motion** project and is commonly used through the `motion` package.

## ✨ Key Features

* Declarative animations
* Enter and exit animations
* Gestures and drag interactions
* Scroll-based animations
* Layout animations
* Spring animations
* Shared layout transitions
* Animation orchestration

## ⚙️ Installation

```bash
npm install motion
```

## 🧪 Basic Example

```jsx
import { motion } from "motion/react";

function App() {
  return (
    <motion.div
      initial={{ opacity: 0, y: 20 }}
      animate={{ opacity: 1, y: 0 }}
      transition={{ duration: 0.5 }}
    >
      Hello Motion
    </motion.div>
  );
}
```

## 🧠 Key Concepts

* **`initial`** — Defines the starting state.
* **`animate`** — Defines the target animated state.
* **`exit`** — Defines the state when an element leaves.
* **`transition`** — Controls timing, easing, and spring behavior.
* **`whileHover`** — Animates during hover.
* **`whileTap`** — Animates during interaction.
* **`whileInView`** — Triggers animations when an element enters the viewport.

## 🎯 Best Used For

* Landing pages
* Portfolio websites
* Page transitions
* Micro-interactions
* Scroll animations
* Interactive UI
* Creative websites

## ⚠️ Keep in Mind

Motion is primarily designed for **React and modern web UI animation**. For highly complex timeline-based animations or advanced canvas/WebGL work, other tools may be more appropriate.

## 📚 Useful Resources

* Documentation: https://motion.dev/docs
* Examples: https://motion.dev/examples
* GitHub: https://github.com/motiondivision/motion
