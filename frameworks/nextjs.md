# Next.js

> A React framework for building full-stack web applications with routing, rendering, data fetching, APIs, optimization, and deployment features built in.

## 🔗 Links

* **Website:** https://nextjs.org/
* **Documentation:** https://nextjs.org/docs
* **Learn Next.js:** https://nextjs.org/learn
* **GitHub:** https://github.com/vercel/next.js

## 📌 What is Next.js?

Next.js is a **React framework** that extends React with features needed to build production-ready web applications.

Instead of combining React with separate tools for routing, rendering, optimization, and server-side functionality, Next.js provides many of these capabilities as part of the framework.

```text
React
  +
Routing
  +
Rendering
  +
Data Fetching
  +
Server Features
  +
Optimization
  ↓
Next.js
```

## ✨ Key Features

* File-system based routing
* App Router
* Server Components
* Client Components
* Server-side rendering (SSR)
* Static rendering
* Dynamic rendering
* Data fetching
* Caching and revalidation
* Route Handlers / API endpoints
* Server Actions
* Nested layouts
* Loading and error UI
* Image optimization
* Font optimization
* Metadata and SEO support
* Middleware / Proxy capabilities
* Full-stack application support

## 🧭 App Router

The **App Router** is the modern routing system in Next.js.

It uses the `app/` directory to define routes and supports features such as:

* Layouts
* Nested routes
* Loading states
* Error handling
* Server Components
* Streaming
* Route Handlers

Example:

```text
app/
├── layout.tsx
├── page.tsx
├── about/
│   └── page.tsx
├── dashboard/
│   ├── layout.tsx
│   └── page.tsx
└── api/
    └── users/
        └── route.ts
```

This produces routes such as:

```text
/               → Home
/about          → About
/dashboard      → Dashboard
/api/users      → API endpoint
```

## 🖥️ Server & Client Components

Next.js App Router uses **Server Components by default**.

Server Components are useful when you need to:

* Fetch data on the server
* Access server-side resources
* Keep sensitive logic on the server
* Reduce unnecessary client-side JavaScript

When a component needs browser functionality or React client-side interactivity, use:

```tsx
"use client";
```

Example:

```tsx
"use client";

import { useState } from "react";

export default function Counter() {
  const [count, setCount] = useState(0);

  return (
    <button onClick={() => setCount(count + 1)}>
      {count}
    </button>
  );
}
```

## 🎨 Styling

Next.js supports multiple styling approaches, including:

* CSS
* CSS Modules
* Tailwind CSS
* Sass
* CSS-in-JS solutions

This makes it easy to combine Next.js with UI libraries such as **shadcn/ui**, **Ant Design**, and other component systems.

## ⚡ Rendering

Next.js can render content using different strategies depending on the application's requirements.

### Static Rendering

Pages can be generated ahead of time and reused for multiple users.

Useful for:

* Blogs
* Documentation
* Marketing pages
* Portfolio websites

### Dynamic Rendering

Content can be generated when a request is made.

Useful for:

* Dashboards
* Personalized pages
* Frequently changing data
* User-specific content

### Streaming

Next.js can stream UI progressively instead of waiting for an entire page to finish rendering.

This can improve perceived loading performance for complex pages.

## 🔄 Data Fetching

Next.js provides several ways to fetch and work with data.

For example, a Server Component can fetch data directly:

```tsx
export default async function Page() {
  const response = await fetch("https://api.example.com/users");
  const users = await response.json();

  return <div>{users.length} users</div>;
}
```

Next.js also provides caching and revalidation mechanisms for controlling how fetched data is reused and updated.

## 🔌 Route Handlers

Next.js can also handle backend-style HTTP endpoints inside the application.

Example:

```text
app/
└── api/
    └── users/
        └── route.ts
```

```tsx
export async function GET() {
  return Response.json({
    message: "Hello from Next.js",
  });
}
```

This makes it possible to build frontend and backend functionality within the same project.

## 📝 Server Actions

Server Actions allow server-side functions to be called from the application, particularly useful for mutations such as:

* Creating records
* Updating data
* Deleting data
* Processing forms

They can reduce the need to manually create API endpoints for certain server-side operations.

## 🖼️ Built-in Optimization

Next.js includes optimization features for common web performance problems.

Examples include:

* `next/image` for image optimization
* `next/font` for font optimization
* Automatic code splitting
* Link prefetching
* Streaming
* Caching

These features help applications achieve better performance without requiring every optimization to be configured manually.

## 🎯 Best Used For

* Full-stack React applications
* SaaS applications
* Dashboards
* E-commerce websites
* Blogs
* Documentation websites
* Marketing websites
* Portfolio websites
* Applications requiring SEO
* Applications combining frontend and backend functionality

## ⚠️ Keep in Mind

Next.js is more opinionated and complex than using React alone.

You should understand:

* JavaScript / TypeScript
* React fundamentals
* Components
* Hooks
* Routing concepts
* Server vs client execution

before trying to use all of its advanced features.

Also, when working with the App Router, understanding **Server Components vs Client Components** is particularly important.

## 🧠 Key Idea

Think of Next.js as the layer that turns React from a UI library into a more complete application framework.

```text
React
  ↓
UI Components

Next.js
  ↓
React
  +
Routing
  +
Rendering
  +
Data
  +
Server Logic
  +
Optimization
  +
Deployment
```

## 📚 Useful Resources

* **Documentation:** https://nextjs.org/docs
* **Learn Next.js:** https://nextjs.org/learn
* **GitHub:** https://github.com/vercel/next.js
