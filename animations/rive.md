# Rive

> A real-time interactive animation platform for creating and embedding lightweight animations in applications and websites.

## 🔗 Links

* **Website:** https://rive.app/
* **Documentation:** https://rive.app/docs/
* **GitHub:** https://github.com/rive-app

## 📌 What is Rive?

Rive is a design and animation platform for creating interactive animations that can run in real time across different platforms.

Unlike traditional exported animations, Rive animations can respond to **user interactions, application state, and inputs** at runtime.

## ✨ Key Features

* Interactive animations
* State machines
* Real-time rendering
* Vector-based graphics
* Lightweight runtime
* Cross-platform support
* Web integration
* React support

## 🧠 Key Concept

Rive separates the **animation/design** from the **application logic**.

```text
Rive Design
     ↓
State Machine
     ↓
Application Input
     ↓
Interactive Animation
```

For example, a button animation could react differently depending on whether the user is hovering, clicking, or completing an action.

## ⚙️ Web Integration

Rive provides a JavaScript runtime for displaying animations on the web.

For React projects, Rive also provides React-specific tooling.

```bash id="q8r2vm"
npm install @rive-app/react-canvas
```

## 🧪 Basic React Example

```jsx id="n4k7xs"
import { useRive } from "@rive-app/react-canvas";

function Animation() {
  const { RiveComponent } = useRive({
    src: "/animation.riv",
    autoplay: true,
  });

  return <RiveComponent />;
}
```

## 🧩 State Machines

One of Rive's most useful features is its **State Machine** system.

It allows animations to transition between states based on inputs.

```text id="p3m6wd"
Idle
 ↓
Hover
 ↓
Active
 ↓
Success
```

This makes Rive particularly useful for interactive UI animations rather than just playing a fixed animation.

## 🎯 Best Used For

* Interactive websites
* Portfolio websites
* Animated buttons
* Interactive illustrations
* Onboarding experiences
* Loading animations
* Product interfaces
* Games and interactive experiences

## ⚠️ Keep in Mind

Rive is more than an animation file format. Its biggest advantage comes from combining **design, animation, and runtime interaction** through state machines.

For simple animations, CSS or Motion may be easier. Rive becomes especially useful when the animation needs to respond dynamically to application state or user input.

## 📚 Useful Resources

* Documentation: https://rive.app/docs/
* Community: https://rive.app/community/
* React Runtime: https://rive.app/docs/runtimes/react
* GitHub: https://github.com/rive-app
