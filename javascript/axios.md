# Axios

> A promise-based HTTP client for making requests from browsers and Node.js applications.

## 🔗 Links

* **Website:** https://axios-http.com/
* **Documentation:** https://axios-http.com/docs/intro
* **GitHub:** https://github.com/axios/axios

## 📌 What is Axios?

Axios is a JavaScript **HTTP client** used to communicate with APIs and web servers.

It simplifies common tasks such as:

* Sending HTTP requests
* Receiving API responses
* Sending JSON data
* Handling errors
* Adding authentication headers
* Cancelling requests
* Intercepting requests and responses

```text
Frontend / Node.js
        ↓
      Axios
        ↓
     HTTP API
        ↓
      Server
```

## ✨ Key Features

* Promise-based API
* Browser and Node.js support
* `GET`, `POST`, `PUT`, `PATCH`, `DELETE`, etc.
* Automatic JSON serialization and parsing
* Request and response interceptors
* Request cancellation
* Timeout support
* Custom Axios instances
* Configurable headers
* Query parameters
* Upload/download progress
* Multiple request adapters

## ⚙️ Installation

```bash
npm install axios
```

## 🚀 Basic GET Request

```javascript
import axios from "axios";

const response = await axios.get(
  "https://api.example.com/users"
);

console.log(response.data);
```

Axios automatically handles the HTTP request and exposes the parsed response through `response.data`.

## 📤 POST Request

```javascript
const response = await axios.post(
  "https://api.example.com/users",
  {
    name: "John",
    email: "john@example.com"
  }
);

console.log(response.data);
```

The second argument contains the request body.

## 🔍 Query Parameters

Instead of manually constructing a URL:

```javascript
axios.get("/users?page=2&limit=10");
```

You can use `params`:

```javascript
axios.get("/users", {
  params: {
    page: 2,
    limit: 10
  }
});
```

Axios handles the parameter serialization for the request.

## 🔐 Headers

Headers can be added to a request:

```javascript
axios.get("/profile", {
  headers: {
    Authorization: "Bearer YOUR_TOKEN"
  }
});
```

This is commonly used for authentication and API authorization.

## 🧩 Axios Instances

Instead of configuring every request individually, you can create a reusable Axios instance.

```javascript
const api = axios.create({
  baseURL: "https://api.example.com",
  timeout: 5000
});

const response = await api.get("/users");
```

This is especially useful when an application communicates with the same API repeatedly.

```text
Axios Instance
    ↓
baseURL
headers
timeout
other defaults
    ↓
Reusable API Client
```

## 🔄 Interceptors

Interceptors allow you to run code before a request is sent or before a response is handled.

### Request Interceptor

```javascript
api.interceptors.request.use((config) => {
  config.headers.Authorization = `Bearer ${token}`;

  return config;
});
```

Useful for:

* Adding authentication tokens
* Logging requests
* Modifying request configuration
* Adding common headers

### Response Interceptor

```javascript
api.interceptors.response.use(
  (response) => response,
  (error) => {
    console.error(error);
    return Promise.reject(error);
  }
);
```

Useful for:

* Centralized error handling
* Processing responses
* Handling authentication failures
* Logging

## ❌ Error Handling

Axios requests can be handled with `try/catch`:

```javascript
try {
  const response = await axios.get("/users");

  console.log(response.data);
} catch (error) {
  console.error("Request failed:", error);
}
```

You can also inspect information such as the HTTP response status.

## ⏱️ Request Cancellation

Axios supports request cancellation using `AbortController`.

```javascript
const controller = new AbortController();

axios.get("/users", {
  signal: controller.signal
});

controller.abort();
```

`AbortController` is the recommended modern cancellation approach; Axios's older `CancelToken` API is deprecated.

## 🧠 Axios vs Fetch

Modern browsers already provide the native `fetch()` API.

### Fetch

```javascript
const response = await fetch("/api/users");
const data = await response.json();
```

### Axios

```javascript
const response = await axios.get("/api/users");
const data = response.data;
```

Axios provides additional conveniences such as interceptors, instances, configurable defaults, and broader request configuration.

**Axios isn't required for making HTTP requests**—`fetch()` is often enough for smaller applications.

## 🎯 Best Used For

* REST API integration
* React applications
* Next.js applications
* Frontend API clients
* Node.js applications
* Applications with authentication
* Applications making many API requests
* Centralized API configuration

## 🧠 Key Idea

Axios acts as the communication layer between your application and an API.

```text
React / Next.js / JavaScript
            ↓
          Axios
            ↓
       HTTP Request
            ↓
          API
            ↓
       HTTP Response
            ↓
          Axios
            ↓
       Your Application
```

## ⚠️ Keep in Mind

Axios is a **client**, not a backend or database.

It doesn't replace:

* Express
* Firebase
* Appwrite
* PostgreSQL
* MongoDB

It simply makes communication with APIs easier.

Also, don't automatically add Axios to every project. For simple requests, the native `fetch()` API may be completely sufficient.

## 📚 Useful Resources

* **Documentation:** https://axios-http.com/docs/intro
* **GitHub:** https://github.com/axios/axios
* **Request Configuration:** https://axios-http.com/docs/req_config
* **Interceptors:** https://axios-http.com/docs/interceptors
