# Service Workers

> A browser API that runs JavaScript in the background, separate from the web page, enabling features such as offline support, caching, background processing, and push notifications.

## 🔗 Links

* **MDN:** https://developer.mozilla.org/en-US/docs/Web/API/Service_Worker_API
* **web.dev:** https://web.dev/learn/pwa/service-workers
* **Specification:** https://w3c.github.io/ServiceWorker/

## 📌 What is a Service Worker?

A Service Worker is a JavaScript file that runs in the browser **independently of a webpage**.

Unlike normal JavaScript running inside a page, a service worker can continue handling certain browser events even when the associated page isn't currently open.

```text id="y7j2qa"
Web Page
    ↓
Browser
    ↓
Service Worker
    ├── Intercept Requests
    ├── Cache Resources
    ├── Handle Push
    └── Background Tasks
```

Service Workers are one of the core technologies behind **Progressive Web Apps (PWAs)**.

## ✨ Key Features

* Network request interception
* Offline functionality
* Resource caching
* Cache management
* Background processing
* Push notifications
* Network-first / cache-first strategies
* App-shell caching
* PWA support

## ⚙️ Registering a Service Worker

A service worker must first be registered by the webpage.

```javascript id="3j3m5a"
if ("serviceWorker" in navigator) {
  navigator.serviceWorker.register("/sw.js")
    .then(() => {
      console.log("Service Worker registered");
    })
    .catch((error) => {
      console.error("Registration failed:", error);
    });
}
```

The service worker itself can then listen for browser events.

## 🔄 Service Worker Lifecycle

A service worker generally goes through several stages:

```text id="d4x2vv"
Register
   ↓
Install
   ↓
Activate
   ↓
Idle
   ↓
Handle Events
   ↓
Update / Replace
```

### Install

The `install` event is commonly used to cache important resources.

```javascript id="q2i5f7"
self.addEventListener("install", (event) => {
  console.log("Service Worker installing");
});
```

### Activate

The `activate` event is useful for cleanup and taking control of clients.

```javascript id="r6v3h2"
self.addEventListener("activate", (event) => {
  console.log("Service Worker activated");
});
```

## 📦 Caching

One of the most important Service Worker features is controlling cached resources.

```javascript id="q0d8uc"
const CACHE_NAME = "app-cache-v1";

self.addEventListener("install", (event) => {
  event.waitUntil(
    caches.open(CACHE_NAME).then((cache) => {
      return cache.addAll([
        "/",
        "/index.html",
        "/styles.css",
        "/app.js"
      ]);
    })
  );
});
```

This can allow an application to load previously cached resources even when the network isn't available.

## 🌐 Intercepting Network Requests

Service Workers can listen for `fetch` events.

```javascript id="v8a1xk"
self.addEventListener("fetch", (event) => {
  event.respondWith(
    caches.match(event.request).then((cachedResponse) => {
      return cachedResponse || fetch(event.request);
    })
  );
});
```

This is the foundation for implementing different **caching strategies**.

## 🧠 Common Caching Strategies

### Cache First

```text id="8ohm4v"
Request
  ↓
Cache?
 ├── Yes → Return Cache
 └── No  → Network
```

Useful for assets that don't change frequently.

### Network First

```text id="zq1g8w"
Request
  ↓
Network?
 ├── Yes → Return Network + Update Cache
 └── No  → Return Cache
```

Useful when fresh data is more important but offline support is still needed.

### Stale While Revalidate

```text id="s5i2cy"
Request
   ↓
Return Cached Version
   +
Fetch Updated Version
   ↓
Update Cache
```

Useful when fast responses are important and slightly stale content is acceptable.

## 📱 Service Workers + PWA

Service Workers are a major part of Progressive Web Apps.

A PWA can use them to provide:

* Offline experiences
* Cached application resources
* Installable web apps
* Faster repeat visits
* Background capabilities
* Push notifications

```text id="9n5m2x"
Web Application
      +
Web App Manifest
      +
Service Worker
      ↓
Progressive Web App
```

## 🔔 Push Notifications

Service Workers can handle push events even when the webpage isn't currently open.

```javascript id="0r6w8d"
self.addEventListener("push", (event) => {
  event.waitUntil(
    self.registration.showNotification("New Message")
  );
});
```

This makes Service Workers useful for applications that need to notify users about new events.

## 🔐 Security Requirements

Service Workers generally require a **secure context**, meaning HTTPS.

The main exception during development is `localhost`, which browsers treat as a secure development origin for this purpose.

Service Workers are also subject to the browser's same-origin security model.

## 🎯 Best Used For

* Progressive Web Apps
* Offline applications
* Offline-first websites
* Resource caching
* Performance improvements
* Push notifications
* Network request control
* Background web functionality

## ⚠️ Keep in Mind

Service Workers do **not** simply act like a normal JavaScript file.

They:

* Run separately from the page
* Have their own lifecycle
* Can be terminated by the browser when idle
* Have restricted access to some browser APIs
* Require careful cache management
* Should not be treated as a general-purpose background thread

Also, caching everything blindly can cause users to receive outdated content, so caching strategies should be designed carefully.

## 🧠 Key Idea

The easiest way to think about a Service Worker is as a programmable layer **between your web application and the network**.

```text id="m0x7yb"
        Web App
           ↓
    Service Worker
       ↙       ↘
    Cache     Network
       ↘       ↙
        Response
           ↓
        Web App
```

This ability to control requests and cache resources is what makes Service Workers particularly powerful for **offline experiences and PWAs**.

## 📚 Useful Resources

* **MDN Service Worker API:** https://developer.mozilla.org/en-US/docs/Web/API/Service_Worker_API
* **MDN Using Service Workers:** https://developer.mozilla.org/en-US/docs/Web/API/Service_Worker_API/Using_Service_Workers
* **web.dev PWA Guide:** https://web.dev/learn/pwa/service-workers
