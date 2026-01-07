---
sidebar_label: "Navbar"
---

# Navbar

A responsive navigation component that collapses into a hamburger menu on mobile devices.

## Basic Usage

The default navbar includes a brand name and a set of navigation links.

<div className="component-preview">
  <nav className="navbar" style={{ position: 'relative', width: '100%', top: 0 }}>
    <div className="navbar__container">
      <a href="#" className="navbar__brand">BEM Framework</a>
      <button className="navbar__toggle" aria-label="Toggle navigation">
        <span></span>
        <span></span>
        <span></span>
      </button>
      <ul className="navbar__menu">
        <li className="navbar__item">
          <a href="#" className="navbar__link is-active">Home</a>
        </li>
        <li className="navbar__item">
          <a href="#" className="navbar__link">About</a>
        </li>
        <li className="navbar__item">
          <a href="#" className="navbar__link">Services</a>
        </li>
        <li className="navbar__item">
          <a href="#" className="navbar__link">Contact</a>
        </li>
      </ul>
    </div>
  </nav>
</div>

```html
<nav class="navbar">
  <div class="navbar__container">
    <a href="#" class="navbar__brand">BEM Framework</a>

    <button class="navbar__toggle" aria-label="Toggle navigation">
      <span></span>
      <span></span>
      <span></span>
    </button>

    <ul class="navbar__menu">
      <li class="navbar__item">
        <a href="#" class="navbar__link is-active">Home</a>
      </li>
      <li class="navbar__item">
        <a href="#" class="navbar__link">About</a>
      </li>
      <li class="navbar__item">
        <a href="#" class="navbar__link">Services</a>
      </li>
      <li class="navbar__item">
        <a href="#" class="navbar__link">Contact</a>
      </li>
    </ul>
  </div>
</nav>
```

## Navbar with Logo

The brand area can accommodate both images/SVGs and text.

<div className="component-preview">
  <nav className="navbar" style={{ position: 'relative', width: '100%', top: 0 }}>
    <div className="navbar__container">
      <a href="#" className="navbar__brand">
        <svg width="32" height="32" viewBox="0 0 32 32" fill="none" style={{ marginRight: '8px' }}>
          <rect width="32" height="32" rx="6" fill="#3b82f6" />
          <path d="M16 8L24 16L16 24L8 16L16 8Z" fill="white" />
        </svg>
        <span>MyBrand</span>
      </a>
      <button className="navbar__toggle" aria-label="Toggle navigation">
        <span></span>
        <span></span>
        <span></span>
      </button>
      <ul className="navbar__menu">
        <li className="navbar__item">
          <a href="#" className="navbar__link is-active">Dashboard</a>
        </li>
        <li className="navbar__item">
          <a href="#" className="navbar__link">Projects</a>
        </li>
        <li className="navbar__item">
          <a href="#" className="navbar__link">Team</a>
        </li>
      </ul>
    </div>
  </nav>
</div>

```html
<a href="#" class="navbar__brand">
  <svg width="32" height="32" viewBox="0 0 32 32">...</svg>
  <span>MyBrand</span>
</a>
```

## Modifiers

### Sticky Navbar

Use the `.navbar--sticky` modifier to keep the navbar fixed at the top of the viewport when scrolling.

```html
<nav class="navbar navbar--sticky">
  <div class="navbar__container">
    <a href="#" class="navbar__brand">Sticky Nav</a>
    <!-- ... -->
  </div>
</nav>
```

### Transparent Navbar

The `.navbar--transparent` modifier is ideal for hero sections with gradient or image backgrounds. It removes the background and adjusts text colors for better contrast.

<div className="component-preview" style={{ padding: 0 }}>
  <div style={{ background: '#333', width: '100%', padding: '2rem 1rem' }}>
    <nav className="navbar navbar--transparent" style={{ position: 'relative', top: 0 }}>
      <div className="navbar__container">
        <a href="#" className="navbar__brand">Transparent</a>
        <ul className="navbar__menu">
          <li className="navbar__item">
            <a href="#" className="navbar__link is-active">Home</a>
          </li>
          <li className="navbar__item">
            <a href="#" className="navbar__link">Features</a>
          </li>
        </ul>
      </div>
    </nav>
    <div style={{ padding: '2rem', color: 'white', textAlign: 'center', height: '200px', overflowY: 'scroll' }}>
      <h1>Hero Content</h1>
      <p>Beautiful transparent navbar over gradient</p>
      <p>Scroll down to see the effect</p>
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
      <p>Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</p>
      <p>Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.</p>
      <p>Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
      <p>Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium.</p>
      <p>Totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo.</p>
      <p>Nemo enim ipsam voluptatem quia voluptas sit aspernatur aut odit aut fugit, sed quia consequuntur magni dolores.</p>
      <p>Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit.</p>
    </div>
  </div>
</div>

```html
<nav class="navbar navbar--transparent">
  <div class="navbar__container">
    <a href="#" class="navbar__brand">Transparent</a>
    <!-- ... -->
  </div>
</nav>
```

## Sizes

### Small Navbar

Use `.navbar--sm` for a more compact navigation bar with reduced padding.

<div className="component-preview">
  <nav className="navbar navbar--sm" style={{ position: 'relative', width: '100%', top: 0 }}>
    <div className="navbar__container">
      <a href="#" className="navbar__brand">Small Nav</a>
      <ul className="navbar__menu">
        <li className="navbar__item">
          <a href="#" className="navbar__link is-active">Home</a>
        </li>
        <li className="navbar__item">
          <a href="#" className="navbar__link">Link</a>
        </li>
      </ul>
    </div>
  </nav>
</div>

```html
<nav class="navbar navbar--sm">...</nav>
```

### Large Navbar

Use `.navbar--lg` for a more spacious navigation bar with increased padding.

<div className="component-preview">
  <nav className="navbar navbar--lg" style={{ position: 'relative', width: '100%', top: 0 }}>
    <div className="navbar__container">
      <a href="#" className="navbar__brand">Large Nav</a>
      <ul className="navbar__menu">
        <li className="navbar__item">
          <a href="#" className="navbar__link is-active">Home</a>
        </li>
        <li className="navbar__item">
          <a href="#" className="navbar__link">Link</a>
        </li>
      </ul>
    </div>
  </nav>
</div>

```html
<nav class="navbar navbar--lg">...</nav>
```

## Combined Modifiers

Modifiers can be combined to achieve specific layouts, such as a sticky transparent navbar.

```html
<nav class="navbar navbar--sticky navbar--transparent">
  <!-- Content -->
</nav>
```

## JavaScript Integration

The navbar requires a small amount of JavaScript to toggle the mobile menu. It uses the `is-active` state class on both the toggle button and the menu.

```javascript
document.addEventListener("DOMContentLoaded", function () {
  const toggleButtons = document.querySelectorAll(".navbar__toggle");

  toggleButtons.forEach((button) => {
    button.addEventListener("click", function () {
      // Toggle button active state (hamburger -> X)
      this.classList.toggle("is-active");

      // Find the menu in the same navbar
      const navbar = this.closest(".navbar");
      const menu = navbar.querySelector(".navbar__menu");

      // Toggle menu active state (show/hide)
      if (menu) {
        menu.classList.toggle("is-active");
      }
    });
  });
});
```

:::tip Implementation Note
Ensure that your CSS targets the `.is-active` class to reveal the `.navbar__menu` on mobile screens and to animate the `.navbar__toggle` icon.
:::
