# Liveblocks

> A platform for building real-time and collaborative features into web applications.

## 🔗 Links

* **Website:** https://liveblocks.io/
* **Documentation:** https://liveblocks.io/docs
* **GitHub:** https://github.com/liveblocks

## 📌 What is Liveblocks?

Liveblocks provides infrastructure and APIs for building **real-time collaborative experiences** into web applications.

It handles much of the complexity involved in synchronizing state and user activity between multiple clients.

## ✨ Key Features

* Real-time collaboration
* Presence
* Shared state
* Multiplayer experiences
* Comments
* Notifications
* Cursors
* Room-based architecture
* Real-time data synchronization

## 🧠 Key Concepts

### Rooms

A room represents a shared real-time environment where users can interact.

```text id="x2v7pn"
User A ──┐
         │
User B ──┼──→ Liveblocks Room
         │
User C ──┘
```

### Presence

Tracks information about users currently connected to a room.

Examples include:

* Cursor position
* Current selection
* Online status
* Active user

### Storage

Allows users in a room to share and synchronize application state.

### Comments

Liveblocks provides infrastructure for adding collaborative commenting features.

## ⚙️ Installation

For a React project:

```bash id="p6k3rm"
npm install @liveblocks/client @liveblocks/react
```

## 🧪 Basic Example

```jsx id="w4n8qs"
import { RoomProvider } from "@liveblocks/react";

function App() {
  return (
    <RoomProvider id="my-room">
      <CollaborativeApp />
    </RoomProvider>
  );
}
```

## 🎯 Best Used For

* Collaborative editors
* Whiteboards
* Design tools
* Multiplayer applications
* Shared dashboards
* Real-time comments
* Presence indicators
* Collaborative SaaS applications

## ⚠️ Keep in Mind

Liveblocks provides the infrastructure for real-time collaboration, but your application still needs to define how the shared state and interactions should behave.

It is most valuable when multiple users need to **see or interact with the same application state in real time**.

## 📚 Useful Resources

* Documentation: https://liveblocks.io/docs
* React Documentation: https://liveblocks.io/docs/api-reference/liveblocks-react
* Examples: https://liveblocks.io/examples
* GitHub: https://github.com/liveblocks
