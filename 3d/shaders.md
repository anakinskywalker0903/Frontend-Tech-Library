# Shaders

> A visual design platform for creating production-ready WebGPU effects without needing to write shader code from scratch.

## 🔗 Links

* **Website:** https://shaders.com/
* **Documentation:** https://shaders.com/docs/guide
* **JavaScript:** https://shaders.com/javascript
* **React:** https://shaders.com/react

## 📌 What is Shaders?

Shaders is a **WebGPU design platform** that lets developers and designers create interactive GPU effects using reusable components.

Instead of manually writing GLSL or WGSL shaders, you can compose visual layers in an editor and export them as code. ([shaders.com](https://shaders.com/docs/guide))

## ✨ Key Features

* WebGPU effects
* Visual shader editor
* 200+ shader components
* Interactive effects
* Image effects
* Cursor effects
* Glass effects
* Distortion
* Lighting
* Procedural shapes
* AI / MCP integration
* Framework exports

## ⚛️ Framework Support

Shaders provides integrations for:

* React
* Vue
* Svelte
* Solid
* JavaScript
* Framer

React and Next.js are supported directly. ([shaders.com](https://shaders.com/react))

## ⚙️ Installation

```bash
npm install shaders
```

Example:

```tsx
import {
  Shader,
  LinearGradient,
  CursorTrail
} from "shaders/react";

export default function Example() {
  return (
    <Shader className="w-full h-64">
      <LinearGradient
        colorA="#0f172a"
        colorB="#7c3aed"
      />
      <CursorTrail />
    </Shader>
  );
}
```

The components are rendered together on a canvas and composited on the GPU. ([shaders.com](https://shaders.com/docs/guide/react/quickstart))

## 🎯 Best Used For

* Creative websites
* Hero backgrounds
* Portfolio websites
* Interactive landing pages
* WebGPU experiments
* Cursor effects
* Glass effects
* Image effects
* Distortion effects

## 🧠 Key Idea

```text
Shader Components
       ↓
Compose Layers
       ↓
WebGPU
       ↓
Interactive Visual
```

You can build sophisticated GPU visuals without having to start by writing shader code manually.

## 📚 Useful Resources

* **Website:** https://shaders.com/
* **Documentation:** https://shaders.com/docs/guide
* **React:** https://shaders.com/react
* **JavaScript:** https://shaders.com/javascript
