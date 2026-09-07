# Matter.js

> A lightweight 2D physics engine for the web, written in JavaScript.

## 🔗 Links

* **Website:** https://brm.io/matter-js/
* **Documentation:** https://brm.io/matter-js/docs/
* **GitHub:** https://github.com/liabru/matter-js

## 📌 What is Matter.js?

Matter.js is a **2D physics engine** written in JavaScript.

It provides the physics calculations needed to create interactive simulations where objects can:

* Move
* Fall
* Collide
* Rotate
* Bounce
* React to forces
* Connect using constraints

Instead of manually calculating physics, Matter.js handles the simulation for you.

```text
Objects
   ↓
Physics Engine
   ↓
Gravity + Forces + Collisions
   ↓
Realistic 2D Motion
```

## ✨ Key Features

* 2D rigid-body physics
* Gravity
* Collision detection
* Friction
* Restitution / bouncing
* Velocity and acceleration
* Constraints
* Sensors
* Compound bodies
* Collision filtering
* Sleeping bodies
* Canvas rendering support

## 🧩 Core Concepts

### World

The world contains the physical objects participating in the simulation.

### Bodies

Bodies represent physical objects.

```javascript
const box = Bodies.rectangle(400, 200, 80, 80);
```

A body can have properties such as:

* Position
* Velocity
* Mass
* Friction
* Restitution
* Angle

### Engine

The engine runs the physics simulation.

```javascript
const engine = Engine.create();
```

### Runner

A runner continuously updates the physics engine.

```javascript
const runner = Runner.create();

Runner.run(runner, engine);
```

### Constraints

Constraints connect bodies together.

They can be used to create:

* Ropes
* Springs
* Hinges
* Joints
* Chains

## ⚙️ Basic Setup

Install Matter.js:

```bash
npm install matter-js
```

Basic example:

```javascript
import Matter from "matter-js";

const {
  Engine,
  Render,
  Runner,
  Bodies,
  Composite
} = Matter;

const engine = Engine.create();

const render = Render.create({
  element: document.body,
  engine: engine
});

const box = Bodies.rectangle(400, 200, 80, 80);

const ground = Bodies.rectangle(
  400,
  400,
  810,
  60,
  { isStatic: true }
);

Composite.add(engine.world, [box, ground]);

Render.run(render);

const runner = Runner.create();
Runner.run(runner, engine);
```

The box will fall onto the ground because of gravity.

## 🎮 What Can You Build?

Matter.js can be used for interactive experiences such as:

* Physics-based games
* Interactive backgrounds
* Drag-and-drop physics
* Bouncing objects
* Falling animations
* Particle-like interactions
* Physics-based UI experiments
* Interactive landing pages
* Creative coding experiments

## 🎨 Matter.js + Creative Websites

Matter.js becomes particularly interesting when combined with frontend animation.

For example:

```text
User Interaction
      ↓
Matter.js Physics
      ↓
Objects respond naturally
      ↓
Visual Animation
```

You could create effects such as:

* UI elements falling onto the screen
* Cards colliding with each other
* Physics-based menus
* Draggable objects
* Interactive hero sections

It can also be combined with libraries such as **React**, **Three.js**, or **GSAP** for more complex experiences.

## 🧠 Key Idea

Matter.js handles the **physics**, while your rendering layer handles how that physics is displayed.

```text
Matter.js
    ↓
Physics State
    ↓
Position / Rotation / Collision
    ↓
Canvas / DOM / WebGL
    ↓
Visual Experience
```

## 🎯 Best Used For

* 2D physics simulations
* Browser games
* Interactive websites
* Creative coding
* Physics-based animations
* Experimental UI
* Interactive landing pages

## ⚠️ Keep in Mind

Matter.js is a **2D** physics engine.

If you need full 3D physics, you'll want a different solution such as a 3D physics engine used alongside WebGL/Three.js.

Also, Matter.js calculates the physics—it doesn't automatically create a polished visual experience. You'll usually combine it with a rendering or animation layer.

## 📚 Useful Resources

* **Website:** https://brm.io/matter-js/
* **Documentation:** https://brm.io/matter-js/docs/
* **GitHub:** https://github.com/liabru/matter-js
