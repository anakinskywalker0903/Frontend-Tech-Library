# Motion One

> A lightweight JavaScript animation library for creating performant animations on the web.

## 🔗 Links

* **Website:** https://motion.dev/
* **Documentation:** https://motion.dev/docs
* **GitHub:** https://github.com/motiondivision/motion

## 📌 What is Motion One?

Motion One was a lightweight animation library built around the **Web Animations API (WAAPI)**.

It provided a simple API for creating performant animations without requiring a large animation framework.

Motion One later evolved into the broader **Motion** project, which now provides animation tools for JavaScript and React.

## ✨ Key Features

* Lightweight animation API
* Web Animations API
* Hardware-accelerated animations
* Keyframe animations
* Spring animations
* Timeline animations
* Gestures and interactions
* Scroll-based animations

## 🧠 Key Idea

Motion provides a simple way to animate DOM elements using JavaScript.

```text id="n7x3qp"
JavaScript
    ↓
Motion
    ↓
Web Animations API
    ↓
Browser
    ↓
Animated DOM
```

## ⚙️ Installation

The current Motion package can be installed with:

```bash id="k5r8vm"
npm install motion
```

## 🧪 Basic Example

```javascript id="p2w6zs"
import { animate } from "motion";

animate(
  ".box",
  { opacity: [0, 1], x: [-100, 0] },
  { duration: 0.5 }
);
```

## 🧩 React

Motion also provides React APIs:

```bash id="m4q9kd"
npm install motion
```

```jsx id="x8v2nr"
import { motion } from "motion/react";

function App() {
  return (
    <motion.div
      initial={{ opacity: 0 }}
      animate={{ opacity: 1 }}
    >
      Hello Motion
    </motion.div>
  );
}
```

## 🎯 Best Used For

* UI animations
* Micro-interactions
* Page transitions
* Hover animations
* Scroll animations
* React animations
* Lightweight web animations

## ⚠️ Keep in Mind

**Motion One is an older name/project in the Motion ecosystem.**

For new projects, use the current **Motion** documentation and package rather than starting a new project specifically around the old `@motionone/*` packages.

## 📚 Useful Resources

* Motion Documentation: https://motion.dev/docs
* JavaScript Animation: https://motion.dev/docs/animate
* React: https://motion.dev/docs/react
* GitHub: https://github.com/motiondivision/motion
