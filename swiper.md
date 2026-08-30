# Swiper

> A modern mobile-friendly slider and carousel library for websites and web applications.

## 🔗 Links

* **Website:** https://swiperjs.com/
* **Documentation:** https://swiperjs.com/get-started
* **GitHub:** https://github.com/nolimits4web/swiper

## 📌 What is Swiper?

Swiper is a touch-enabled slider and carousel library for modern web applications.

It supports touch gestures, responsive layouts, animations, navigation, pagination, and many other features needed to build interactive sliders.

## ✨ Key Features

* Touch and swipe gestures
* Responsive sliders
* Carousel layouts
* Navigation controls
* Pagination
* Autoplay
* Looping
* Keyboard control
* Mousewheel support
* Responsive breakpoints
* Multiple slides per view

## 🧩 Framework Support

Swiper provides integrations for:

* JavaScript
* React
* Vue
* Svelte
* Angular
* Web Components

## ⚙️ Installation

```bash id="g5r8pk"
npm install swiper
```

## 🧪 Basic HTML Example

```html id="v3m9qx"
<div class="swiper">
  <div class="swiper-wrapper">
    <div class="swiper-slide">Slide 1</div>
    <div class="swiper-slide">Slide 2</div>
    <div class="swiper-slide">Slide 3</div>
  </div>

  <div class="swiper-pagination"></div>
</div>
```

## ⚛️ React Example

```jsx id="p7k2wd"
import { Swiper, SwiperSlide } from "swiper/react";
import "swiper/css";

function App() {
  return (
    <Swiper>
      <SwiperSlide>Slide 1</SwiperSlide>
      <SwiperSlide>Slide 2</SwiperSlide>
      <SwiperSlide>Slide 3</SwiperSlide>
    </Swiper>
  );
}
```

## 🧠 Common Features

### Autoplay

Automatically moves through slides.

### Navigation

Provides previous and next controls.

### Pagination

Displays indicators for the current slide.

### Breakpoints

Allows the number of visible slides to change based on screen size.

```text id="w6n4sz"
Desktop → 3 slides
Tablet  → 2 slides
Mobile  → 1 slide
```

## 🎯 Best Used For

* Image galleries
* Product carousels
* Testimonials
* Portfolio projects
* Hero sliders
* Product showcases
* Mobile interfaces
* Content carousels

## ⚠️ Keep in Mind

Swiper provides many features out of the box, but for a very simple slider it may be more functionality than you need.

For highly custom animation-driven sliders, combining a lower-level animation library with your own carousel logic may provide more control.

## 📚 Useful Resources

* Documentation: https://swiperjs.com/get-started
* Demos: https://swiperjs.com/demos
* React: https://swiperjs.com/react
* API: https://swiperjs.com/swiper-api
* GitHub: https://github.com/nolimits4web/swiper
