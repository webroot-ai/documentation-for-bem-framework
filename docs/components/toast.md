---
sidebar_label: "Toast"
---

# Toast

Toasts are lightweight notifications designed to mimic the push notifications that have been popularized by mobile and desktop operating systems.

## Basic Usage

Toasts are fixed-position elements that usually appear in a corner of the screen.

<div className="component-preview component-preview--center" style={{padding: '20px', background: '#f8fafc', position: 'relative', height: '150px'}}>
  <div className="toast" style={{position: 'absolute', top: '20px', left: '50%', transform: 'translateX(-50%)'}}>
    <div className="toast__content">
      <h4 className="toast__title">Notification</h4>
      <p className="toast__description">This is a default toast message.</p>
    </div>
    <button className="toast__close" aria-label="Close">×</button>
  </div>
</div>

```html
<div class="toast" role="alert" aria-live="assertive">
  <div class="toast__content">
    <h4 class="toast__title">Notification</h4>
    <p class="toast__description">This is a default toast message.</p>
  </div>
  <button class="toast__close" aria-label="Close">×</button>
</div>
```

## Variants

<div className="component-preview component-preview--column">
  <div className="toast toast--info" style={{position: 'static'}}>
    <div className="toast__icon">ℹ️</div>
    <div className="toast__content">
      <h4 className="toast__title">Info Toast</h4>
      <p className="toast__description">New update available.</p>
    </div>
    <div className="toast__progress"></div>
  </div>

  <div className="toast toast--success" style={{position: 'static'}}>
    <div className="toast__icon">✓</div>
    <div className="toast__content">
      <h4 className="toast__title">Success Toast</h4>
      <p className="toast__description">Changes saved successfully.</p>
    </div>
  </div>

  <div className="toast toast--warning" style={{position: 'static'}}>
     <div className="toast__icon">⚠️</div>
     <div className="toast__content">
      <h4 className="toast__title">Warning Toast</h4>
      <p className="toast__description">Your session is about to expire.</p>
    </div>
  </div>

  <div className="toast toast--error" style={{position: 'static'}}>
     <div className="toast__icon">❌</div>
    <div className="toast__content">
      <h4 className="toast__title">Error Toast</h4>
      <p className="toast__description">Failed to save changes.</p>
    </div>
  </div>
</div>

```html
<div class="toast toast--info">
  <div class="toast__icon">ℹ️</div>
  <div class="toast__content">...</div>
  <div class="toast__progress"></div>
</div>

<div class="toast toast--success">...</div>
<div class="toast toast--warning">...</div>
<div class="toast toast--error">...</div>
```

## Positions

Toasts are positioned using modifiers, which set `position: fixed`.

- `.toast--top-right` (default)
- `.toast--top-left`
- `.toast--bottom-right`
- `.toast--bottom-left`
- `.toast--top-center`
- `.toast--bottom-center`

```html
<div class="toast toast--top-right">...</div>
```

## Toast Container

When displaying multiple toasts, wrap them in a `.toast-container` to handle stacking.

```html
<div class="toast-container toast-container--top-right">
  <div class="toast toast--success">...</div>
  <div class="toast toast--info">...</div>
</div>
```

## Sizes

### Small

<div className="component-preview component-preview--center">
  <div className="toast toast--sm" style={{position: 'static'}}>
    <div className="toast__content">
      <h4 className="toast__title">Small Toast</h4>
      <p className="toast__description">Compact notification.</p>
    </div>
  </div>
</div>

```html
<div class="toast toast--sm">...</div>
```

### Large

<div className="component-preview component-preview--center">
  <div className="toast toast--lg" style={{position: 'static'}}>
    <div className="toast__content">
      <h4 className="toast__title">Large Toast</h4>
      <p className="toast__description">Detailed notification.</p>
    </div>
  </div>
</div>

```html
<div class="toast toast--lg">...</div>
```
