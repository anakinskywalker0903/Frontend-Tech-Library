# PostCSS

> A tool for transforming CSS using JavaScript plugins.

## 🔗 Links

* **Website:** https://postcss.org/
* **Documentation:** https://postcss.org/docs/
* **GitHub:** https://github.com/postcss/postcss

## 📌 What is PostCSS?

PostCSS is a tool that **parses CSS and transforms it using JavaScript plugins**.

PostCSS itself doesn't provide a specific CSS framework or styling system. Instead, it provides a plugin-based system that allows developers and tools to process CSS.

```text
CSS
 ↓
PostCSS
 ↓
Plugins
 ↓
Transformed CSS
 ↓
Browser
```

## 🧩 How It Works

PostCSS uses plugins to modify or analyze CSS.

For example:

```text
Input CSS
   ↓
PostCSS
   ↓
Autoprefixer
   ↓
CSS transformed for browser compatibility
   ↓
Output CSS
```

This makes PostCSS more of a **CSS processing platform** than a single-purpose tool.

## ✨ Key Features

* Plugin-based architecture
* CSS transformation
* CSS parsing
* Browser compatibility processing
* Custom CSS transformations
* Integration with build tools
* Extensible through JavaScript plugins

## 🔌 Popular Plugins

### Autoprefixer

Automatically adds vendor prefixes when necessary.

Example:

```css
.example {
  user-select: none;
}
```

Can become:

```css
.example {
  -webkit-user-select: none;
  user-select: none;
}
```

Autoprefixer determines which prefixes are required based on your browser support configuration.

### PostCSS Preset Env

Allows developers to use modern CSS features while transforming them for supported browser environments.

### CSS Modules

PostCSS can also be integrated into workflows involving CSS Modules and other CSS processing systems.

## ⚙️ Installation

Install PostCSS:

```bash
npm install postcss
```

A common setup also includes the PostCSS CLI:

```bash
npm install postcss-cli
```

Plugins are installed separately depending on what transformations you need.

For example:

```bash
npm install autoprefixer
```

## 🛠️ Configuration

PostCSS can be configured using a `postcss.config.js` file.

Example:

```javascript
module.exports = {
  plugins: [
    require("autoprefixer")
  ]
};
```

The exact configuration can vary depending on your build tool and project setup.

## 🔗 PostCSS + Build Tools

PostCSS is commonly integrated into modern frontend build systems.

```text
Source CSS
    ↓
PostCSS
    ↓
Plugins
    ↓
Bundler / Build Tool
    ↓
Production CSS
```

It can work alongside tools such as:

* Vite
* webpack
* Parcel
* Rollup
* Next.js

## 🎯 Best Used For

* CSS transformations
* Browser compatibility
* Automated vendor prefixes
* CSS processing pipelines
* Custom CSS tooling
* Build-time CSS optimization
* Modern frontend build systems

## 🧠 Key Idea

**PostCSS is not a CSS framework.**

Think of it as a **JavaScript-powered CSS processing pipeline**.

```text
PostCSS
   │
   ├── Parse CSS
   │
   ├── Run Plugins
   │      ├── Autoprefixer
   │      ├── Preset Env
   │      └── Custom Plugins
   │
   └── Generate CSS
```

The power of PostCSS comes primarily from its **plugin ecosystem**.

## ⚠️ Keep in Mind

PostCSS by itself doesn't automatically make your CSS better or add features.

You generally use it together with plugins that perform specific transformations.

Also, many modern frameworks and build tools already configure PostCSS internally, so you may not always need to configure it manually.

## 📚 Useful Resources

* **Documentation:** https://postcss.org/docs/
* **GitHub:** https://github.com/postcss/postcss
* **Plugin Directory:** https://www.postcss.parts/

