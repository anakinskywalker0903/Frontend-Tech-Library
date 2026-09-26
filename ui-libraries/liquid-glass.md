# Liquid Glass

> A React component that creates real-time liquid glass and refraction effects using WebGL.

## 🔗 Links

* **Website:** https://glass.samasante.com/
* **Documentation:** https://glass.samasante.com/?view=docs

## 📌 What is Liquid Glass?

Liquid Glass is a React component that creates a **glass/refraction effect over live HTML content**.

Instead of using only CSS properties such as `backdrop-filter`, it uses WebGL to create more realistic visual effects such as:

* Refraction
* Distortion
* Blur
* Magnification
* Rounded glass surfaces
* Interactive glass effects

```text
HTML Content
     ↓
Liquid Glass
     ↓
WebGL Processing
     ↓
Refraction + Distortion
     ↓
Glass UI
```

## ✨ Key Features

* Real-time glass effect
* WebGL-powered rendering
* Live DOM/content refraction
* React component
* Zero external dependencies
* Customizable appearance
* Supports rounded shapes
* Interactive effects
* Works with existing HTML content

## ⚛️ React Usage

The library provides a `Glass` component that can wrap content.

```tsx
import { Glass } from "liquid-glass-react";

export default function Example() {
  return (
    <Glass>
      <div>
        <h2>Hello</h2>
        <p>Liquid glass effect</p>
      </div>
    </Glass>
  );
}
```

Check the official documentation for the current package name and API before installing, as the implementation and API can evolve.

## 🧊 How It Works

Traditional glass effects often rely on CSS:

```css
backdrop-filter: blur(20px);
```

Liquid Glass instead introduces a rendering layer:

```text
Background / DOM
       ↓
   WebGL Canvas
       ↓
Distortion + Refraction
       ↓
   Glass Surface
       ↓
      UI
```

This allows the glass to behave more like a physical optical surface.

## 🎨 Customization

The effect can be customized to control aspects such as:

* Glass size
* Border radius
* Refraction
* Distortion
* Blur
* Magnification
* Surface appearance

This makes it suitable for creating custom glass-style UI rather than relying on a single predefined visual effect.

## 🎯 Best Used For

* Creative websites
* Portfolio websites
* Landing pages
* Hero sections
* Navigation bars
* Floating cards
* Interactive controls
* Apple-inspired interfaces
* Experimental UI
* WebGL experiences

## 🧠 Key Idea

Liquid Glass combines **traditional HTML UI with GPU-powered rendering**.

```text
HTML
 +
React
 +
WebGL
 ↓
Interactive Glass UI
```

The main advantage over a simple CSS glass effect is the ability to create **actual optical-style distortion and refraction**.

## ⚠️ Keep in Mind

Because the effect relies on WebGL, performance and browser/device capabilities should be considered when using it extensively.

It is generally better suited to **specific visual elements** than applying heavy GPU effects to an entire application.

Also provide a suitable fallback for users or environments where the required rendering capabilities aren't available.

## 📚 Useful Resources

* **Website:** https://glass.samasante.com/
* **Documentation:** https://glass.samasante.com/?view=docs
