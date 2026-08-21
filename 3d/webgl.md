# WebGL

> A JavaScript API for rendering interactive 2D and 3D graphics directly in the browser using the GPU.

## 🔗 Links

* **Website:** https://www.khronos.org/webgl/
* **Documentation:** https://developer.mozilla.org/en-US/docs/Web/API/WebGL_API
* **Specification:** https://registry.khronos.org/webgl/

## 📌 What is WebGL?

WebGL (Web Graphics Library) is a browser API that allows JavaScript applications to render hardware-accelerated 2D and 3D graphics without requiring plugins.

It provides access to the GPU through the browser and is based on OpenGL ES.

## ✨ Key Features

* GPU-accelerated graphics
* 2D and 3D rendering
* Runs directly in modern browsers
* Supports custom shaders
* Interactive visualizations
* Real-time graphics

## 🧠 Key Concepts

### Canvas

WebGL renders graphics inside an HTML `<canvas>` element.

### Context

A WebGL context provides the interface for communicating with the GPU.

```javascript id="x0j1q2"
const canvas = document.querySelector("canvas");
const gl = canvas.getContext("webgl");
```

### Shaders

Small programs that run on the GPU.

WebGL primarily uses:

* **Vertex shaders** — process vertices and geometry.
* **Fragment shaders** — determine the color of pixels.

### Buffers

Store geometry and other data that is sent to the GPU.

### Textures

Images or other data mapped onto 3D objects.

## 🔄 Basic Rendering Pipeline

```text id="7l6d9q"
JavaScript
    ↓
WebGL API
    ↓
Vertex Shader
    ↓
Rasterization
    ↓
Fragment Shader
    ↓
GPU
    ↓
Pixels on Canvas
```

## 🎯 Best Used For

* 3D websites
* Interactive experiences
* Data visualization
* Games
* Simulations
* Creative coding
* GPU-accelerated graphics

## ⚠️ Keep in Mind

WebGL is a relatively low-level graphics API. Creating complex 3D experiences directly with WebGL requires understanding concepts such as shaders, buffers, matrices, cameras, lighting, and GPU rendering.

Libraries such as **Three.js** provide a higher-level abstraction over WebGL and make building 3D experiences significantly easier.

## 📚 Useful Resources

* MDN WebGL Guide: https://developer.mozilla.org/en-US/docs/Web/API/WebGL_API
* Khronos WebGL: https://www.khronos.org/webgl/
* WebGL Specification: https://registry.khronos.org/webgl/
