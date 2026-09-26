# vgpu

> A modular TypeScript WebGPU library for graphics, shaders, 3D scenes, GPU computation, and visualization.

## 🔗 Links

* **Website:** https://vgpu.sh/
* **GitHub:** https://github.com/vercel-labs/vgpu

## 📌 What is vgpu?

vgpu is a **TypeScript library for WebGPU** created by Vercel Labs.

It provides a small GPU-first API that can run across multiple environments:

* Browser
* Headless Node.js
* Tests
* Server-side environments

It supports graphics, shaders, 3D scenes, GPU tensors, neural networks, and mathematical visualization. ([github.com](https://github.com/vercel-labs/vgpu))

## ✨ Key Features

* TypeScript-first API
* WebGPU
* Typed WGSL imports
* Browser support
* Node support
* Mock runtime for testing
* GPU effects
* Compute
* 3D scenes
* GPU tensors
* Agent tooling

## ⚙️ Installation

```bash
pnpm add vgpu
pnpm add -D @webgpu/types
```

## 🚀 Basic Example

```typescript
import {
  clock,
  init,
  effect,
  frameLoop,
  surface
} from "vgpu";

const gpu = await init();

const canvasSurface = surface(
  gpu,
  canvas,
  { dpr: [1, 2] }
);

const wave = effect(
  gpu,
  waveShader,
  { set: { speed: 2 } }
);

const time = clock(gpu);

frameLoop(gpu, (frame) => {
  wave.set({ time: time.time });
  frame.pass(canvasSurface, wave);
});
```

## 🎯 Best Used For

* WebGPU applications
* GPU graphics
* Shader development
* 3D experiences
* GPU computation
* Data visualization
* Neural network experiments
* Creative coding

## 🧠 Key Idea

```text
TypeScript
    ↓
vgpu
    ↓
WebGPU
    ↓
GPU
 ├── Graphics
 ├── Shaders
 ├── Compute
 └── Visualization
```

## 📚 Useful Resources

* **Website:** https://vgpu.sh/
* **GitHub:** https://github.com/vercel-labs/vgpu
* **Documentation:** https://vgpu.sh/
