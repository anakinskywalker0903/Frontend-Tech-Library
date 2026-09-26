# SSGOI

> A framework-agnostic page transition library for creating native app-like navigation experiences on the web.

## 🔗 Links

* **Website:** https://ssgoi.dev/
* **Documentation:** https://ssgoi.dev/docs
* **GitHub:** https://github.com/ssgoi-dev/ssgoi

## 📌 What is SSGOI?

SSGOI is a **page transition animation library** that animates the transition between routes without replacing the router or navigation system already used by your application.

It works with multiple frameworks and uses the **Web Animations API** for its animation engine.

```text
Existing Router
      ↓
   SSGOI
      ↓
Route Transition
      ↓
Animated Navigation
```

## ✨ Key Features

* Native-style page transitions
* Framework agnostic
* Web Animations API
* Spring-based motion
* Route-specific transitions
* SSR-friendly
* Preset transitions
* Minimal integration
* No need to replace your existing router

## ⚛️ Framework Support

SSGOI provides packages for:

* React
* Svelte
* Vue
* Solid
* Angular
* Qwik

It also provides guides for frameworks such as Next.js, SvelteKit, and Nuxt.

## 🎬 Transition Presets

The library includes several transition styles, including:

* Drill
* Sheet
* Slide
* Zoom
* Fade
* Film
* Hero
* Rotate
* Strip

Different transitions can communicate different navigation relationships.

For example:

```text
List → Detail
   ↓
Drill / Zoom

Tab → Tab
   ↓
Slide

Focused Action
   ↓
Sheet
```

## ⚙️ Installation

For React:

```bash
npm install @ssgoi/react
```

Other framework-specific packages are also available.

## ⚛️ React Example

```tsx
import { Ssgoi } from "@ssgoi/react";
import { drill } from "@ssgoi/react/view-transitions";

const config = {
  transitions: [
    {
      on: "/**",
      except: "/",
      transition: drill(),
    },
  ],
};
```

The route boundary determines which part of the page participates in the transition.

## 🚀 How It Works

SSGOI doesn't take over routing.

Instead:

```text
Your Router
     ↓
Creates / Removes Route DOM
     ↓
SSGOI observes the transition
     ↓
Animation
     ↓
New Route
```

This allows existing routing, SSR, data loading, history, and prefetching behavior to remain under the framework's control.

## ⚡ Web Animations API

SSGOI 3.0 moved its animation engine toward the **Web Animations API**.

Spring motion can be calculated ahead of time and converted into keyframes that the browser executes, reducing the amount of animation work performed by JavaScript during playback.

## 🎯 Best Used For

* Next.js applications
* React applications
* Svelte applications
* Mobile-style web experiences
* Page transitions
* Portfolio websites
* Creative websites
* Interactive product websites

## 🧠 Key Idea

SSGOI adds **spatial meaning to navigation**.

```text
Navigation
    +
Motion
    ↓
User understands
where they came from
and where they're going
```

Instead of every route simply disappearing and appearing, the transition can communicate the relationship between two screens.

## ⚠️ Keep in Mind

SSGOI is specifically focused on **route/page transitions**.

For general-purpose UI animations, libraries such as Motion, GSAP, or Framer Motion may be more appropriate.

## 📚 Useful Resources

* **Website:** https://ssgoi.dev/
* **Documentation:** https://ssgoi.dev/docs
* **GitHub:** https://github.com/ssgoi-dev/ssgoi
