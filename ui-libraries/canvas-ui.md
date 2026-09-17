# Canvas UI

> An open-source library of creative HTML-in-canvas components powered by WebGL and WebGPU.

## 🔗 Links

* **Website:** https://canvasui.dev/
* **Documentation:** https://canvasui.dev/docs
* **Components:** https://canvasui.dev/components

## 📌 What is Canvas UI?

Canvas UI is a collection of **creative and interactive web components** that combine real HTML with Canvas-based GPU effects.

It focuses on visual experiences such as:

* Fluid effects
* Glass effects
* Particle effects
* Shaders
* Distortion
* Interactive backgrounds
* 3D effects
* Creative cursor interactions

The library is **framework agnostic** and currently provides components for React, Solid, Preact, Vue, Svelte, and vanilla TypeScript.

```text
HTML Content
     ↓
Canvas UI
     ↓
WebGL / WebGPU
     ↓
GPU Effects
     ↓
Interactive UI
```

## ✨ Key Features

* Creative canvas components
* WebGL support
* WebGPU support
* HTML-in-canvas effects
* GPU-powered animations
* Framework agnostic
* Copy-and-customize components
* shadcn-compatible registry
* React, Vue, Svelte, Solid, Preact and vanilla TypeScript
* Reduced-motion support

## 🎨 Components

Canvas UI provides a growing collection of creative effects, including:

* Liquid
* Glass
* Shatter
* Particle Reveal
* Blaze
* Frost
* Ripple
* Clouds
* Displacement
* Glitch
* VHS
* Magnify
* Grid
* Cloth
* Particle Object
* Glass Object
* ASCII Object
* Dithered Object

The library currently lists **35 components and counting**.

## ⚙️ Installation

Canvas UI uses a **shadcn-compatible registry** rather than requiring you to install a traditional component package.

For example:

```bash
npx shadcn@latest add @canvas-ui/particle-reveal-react
```

The component source is copied directly into your project, allowing you to modify and customize it.

## ⚛️ Framework Support

Each component is available in multiple versions:

```text
Canvas UI
   │
   ├── React
   ├── Solid
   ├── Preact
   ├── Vue
   ├── Svelte
   └── Vanilla TypeScript
```

The same component concept and options are maintained across the different frameworks.

## 🖥️ WebGL & WebGPU

Canvas UI provides both **WebGL and WebGPU** renderer builds.

### WebGL

Useful when you want:

* Wider browser support
* GLSL shaders
* Minimal additional dependencies

### WebGPU

Useful when you want:

* WGSL shaders
* WebGPU-native rendering
* Modern GPU capabilities
* Compute-oriented workflows

The two builds expose the same general public API and component options.

## 🧩 Example

A React component can be installed and used like:

```tsx
import { ParticleReveal } from "@/components/canvasui/ParticleReveal";

export function Hero() {
  return (
    <ParticleReveal radius={300}>
      <YourContent />
    </ParticleReveal>
  );
}
```

The component can then be customized directly because its source lives inside your project.

## 🤖 AI / MCP Support

Canvas UI is also designed to work with the **shadcn MCP ecosystem**.

An AI coding assistant can browse the Canvas UI registry, inspect components, and install them into a project.

Example:

```bash
npx shadcn@latest mcp init --client claude
```

The Canvas UI registry can then be used through the shadcn MCP setup.

## 🎯 Best Used For

* Creative portfolio websites
* Agency websites
* Interactive landing pages
* Hero sections
* Experimental UI
* Product websites
* WebGL experiences
* WebGPU experiments
* Interactive backgrounds
* Cursor-based effects
* Animation-heavy websites

## 🧠 Key Idea

Canvas UI sits between **traditional UI components and GPU-powered creative effects**.

```text
Traditional UI
      +
HTML
      +
Canvas
      +
WebGL / WebGPU
      ↓
Creative Interactive UI
```

Instead of building complex shader and canvas effects from scratch, you can start with a ready-made component and customize its source.

## ⚠️ Keep in Mind

Some Canvas UI effects rely on the experimental **HTML-in-canvas** browser capability.

When that capability isn't available, the library is designed to degrade gracefully: the underlying content remains regular HTML while supported GPU effects can continue running as overlays. WebGL generally has broader support than WebGPU.

For components involving 3D models, SVGs, or images, some effects also use **Three.js**.

## 📚 Useful Resources

* **Website:** https://canvasui.dev/
* **Documentation:** https://canvasui.dev/docs
* **Components:** https://canvasui.dev/components
* **Rendering Guide:** https://canvasui.dev/docs/rendering
* **MCP:** https://canvasui.dev/docs/mcp
