# shadcn/ui

> A collection of beautifully designed, accessible React components that you can copy and customize in your own projects.

## 🔗 Links

* **Website:** https://ui.shadcn.com/
* **Documentation:** https://ui.shadcn.com/docs
* **GitHub:** https://github.com/shadcn-ui/ui

## 📌 What is shadcn/ui?

shadcn/ui is a collection of reusable React components built using **Radix UI** and **Tailwind CSS**.

Unlike traditional component libraries, shadcn/ui does not work by installing a package of pre-built components that you simply import.

Instead, the component source code is added directly to your project, giving you full control over customization.

## ✨ Key Features

* Accessible components
* Tailwind CSS based
* Highly customizable
* Copy-and-own approach
* TypeScript support
* Built on Radix UI
* Modern component designs
* CLI for adding components

## 🧠 Key Idea

**You own the component code.**

Instead of:

```jsx
import { Button } from "some-library";
```

shadcn/ui adds the component source to your project so you can modify it directly.

## ⚙️ Installation

Initialize shadcn/ui in a project:

```bash
npx shadcn@latest init
```

Add a component:

```bash
npx shadcn@latest add button
```

Then use it:

```jsx
import { Button } from "@/components/ui/button";

<Button>Click me</Button>
```

## 🧩 Components

Some commonly available components include:

* Button
* Card
* Dialog
* Dropdown Menu
* Input
* Select
* Tabs
* Tooltip
* Accordion
* Navigation Menu
* Sheet
* Table
* Form

## 🎯 Best Used For

* React applications
* SaaS dashboards
* Modern web applications
* Admin panels
* Landing pages
* Custom design systems
* Projects requiring highly customizable UI

## ⚠️ Keep in Mind

shadcn/ui is **not a traditional component library**. The components become part of your codebase, so you are responsible for maintaining and customizing them.

It also relies heavily on Tailwind CSS and the modern React/TypeScript ecosystem.

## 📚 Useful Resources

* Documentation: https://ui.shadcn.com/docs
* Components: https://ui.shadcn.com/docs/components
* GitHub: https://github.com/shadcn-ui/ui
