# Appwrite

> An open-source Backend-as-a-Service (BaaS) platform for building web and mobile applications.

## 🔗 Links

* **Website:** https://appwrite.io/
* **Documentation:** https://appwrite.io/docs
* **GitHub:** https://github.com/appwrite/appwrite

## 📌 What is Appwrite?

Appwrite is an open-source backend platform that provides ready-to-use backend services through APIs and SDKs.

It allows developers to build applications without having to create and maintain every backend service from scratch.

## ✨ Key Features

* Authentication
* Databases
* Storage
* Serverless Functions
* Messaging
* Hosting
* Permissions
* APIs
* User management

## 🧩 Core Services

### 🔐 Authentication

Provides user registration, login, sessions, OAuth, and other authentication methods.

### 🗄️ Databases

Provides a database system for storing and querying application data.

### 📦 Storage

Used for uploading and managing files such as images, documents, and videos.

### ⚡ Functions

Allows you to run backend code in response to events or API requests.

### 💬 Messaging

Provides services for sending notifications and messages.

## 🧠 How It Fits Together

```text id="v4m8qs"
Frontend
   ↓
Appwrite SDK
   ↓
┌─────────────────────┐
│      Appwrite       │
├─────────────────────┤
│ Authentication      │
│ Databases           │
│ Storage             │
│ Functions           │
│ Messaging           │
└─────────────────────┘
```

## ⚙️ Installation

For a JavaScript project:

```bash id="n6p2rx"
npm install appwrite
```

## 🧪 Basic Example

```javascript id="k8w4mz"
import { Client } from "appwrite";

const client = new Client();

client
  .setEndpoint("https://<REGION>.cloud.appwrite.io/v1")
  .setProject("<PROJECT_ID>");
```

Appwrite can then be used through its SDKs to interact with backend services.

## 🎯 Best Used For

* Full-stack web applications
* React applications
* Mobile applications
* Authentication systems
* File storage
* Database-backed applications
* Rapid prototyping
* Applications where you want an open-source BaaS option

## ⚠️ Keep in Mind

Appwrite abstracts away many backend responsibilities, which makes development faster but also means your application depends on Appwrite's APIs and architecture.

One of its major advantages is that Appwrite can be **self-hosted**, giving you more control over your backend infrastructure.

## 📚 Useful Resources

* Documentation: https://appwrite.io/docs
* Console: https://cloud.appwrite.io/
* GitHub: https://github.com/appwrite/appwrite
* SDKs: https://appwrite.io/docs/sdks
