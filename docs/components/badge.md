---
sidebar_label: "Badge"
---

# Badge Component

Flexible badge component for labels, notifications, and status indicators.

## Basic Badge

<div className="component-preview component-preview--center">
  <div className="badge-group">
    <span className="badge">Default</span>
    <span className="badge">Label</span>
    <span className="badge">Tag</span>
  </div>
</div>

```html
<span class="badge">Default</span>
<span class="badge">Label</span>
<span class="badge">Tag</span>
```

## Color Variants

<div className="component-preview component-preview--center">
  <div className="badge-group">
    <span className="badge badge--primary">Primary</span>
    <span className="badge badge--secondary">Secondary</span>
    <span className="badge badge--success">Success</span>
    <span className="badge badge--error">Error</span>
    <span className="badge badge--warning">Warning</span>
    <span className="badge badge--info">Info</span>
  </div>
</div>

```html
<span class="badge badge--primary">Primary</span>
<span class="badge badge--secondary">Secondary</span>
<span class="badge badge--success">Success</span>
<span class="badge badge--error">Error</span>
<span class="badge badge--warning">Warning</span>
<span class="badge badge--info">Info</span>
```

## Sizes

<div className="component-preview component-preview--center">
  <div className="badge-group">
    <span className="badge badge--primary badge--xs">Extra Small</span>
    <span className="badge badge--primary badge--sm">Small</span>
    <span className="badge badge--primary badge--md">Medium</span>
    <span className="badge badge--primary badge--lg">Large</span>
  </div>
</div>

```html
<span class="badge badge--primary badge--xs">Extra Small</span>
<span class="badge badge--primary badge--sm">Small</span>
<span class="badge badge--primary badge--md">Medium</span>
<span class="badge badge--primary badge--lg">Large</span>
```

## Shapes

### Pill Shape

<div className="component-preview component-preview--center">
  <div className="badge-group">
    <span className="badge badge--primary badge--pill">Pill</span>
    <span className="badge badge--success badge--pill">Success</span>
    <span className="badge badge--error badge--pill">Error</span>
  </div>
</div>

```html
<span class="badge badge--primary badge--pill">Pill</span>
```

### Rounded Corners

<div className="component-preview component-preview--center">
  <div className="badge-group">
    <span className="badge badge--primary badge--rounded">Rounded</span>
    <span className="badge badge--success badge--rounded">Success</span>
    <span className="badge badge--error badge--rounded">Error</span>
  </div>
</div>

```html
<span class="badge badge--primary badge--rounded">Rounded</span>
```

### Square

<div className="component-preview component-preview--center">
  <div className="badge-group">
    <span className="badge badge--primary badge--square">Square</span>
    <span className="badge badge--success badge--square">Success</span>
    <span className="badge badge--error badge--square">Error</span>
  </div>
</div>

```html
<span class="badge badge--primary badge--square">Square</span>
```

## Styles

### Outline Style

<div className="component-preview component-preview--center">
  <div className="badge-group">
    <span className="badge badge--outline badge--primary">Primary</span>
    <span className="badge badge--outline badge--secondary">Secondary</span>
    <span className="badge badge--outline badge--success">Success</span>
    <span className="badge badge--outline badge--error">Error</span>
    <span className="badge badge--outline badge--warning">Warning</span>
    <span className="badge badge--outline badge--info">Info</span>
  </div>
</div>

```html
<span class="badge badge--outline badge--primary">Primary</span>
```

### Soft Style

<div className="component-preview component-preview--center">
  <div className="badge-group">
    <span className="badge badge--soft badge--primary">Primary</span>
    <span className="badge badge--soft badge--secondary">Secondary</span>
    <span className="badge badge--soft badge--success">Success</span>
    <span className="badge badge--soft badge--error">Error</span>
    <span className="badge badge--soft badge--warning">Warning</span>
    <span className="badge badge--soft badge--info">Info</span>
  </div>
</div>

```html
<span class="badge badge--soft badge--primary">Primary</span>
```

## Notification Badges

<div className="component-preview component-preview--center">
  <div className="badge-group">
    <span className="badge badge--primary badge--notification">3</span>
    <span className="badge badge--error badge--notification">9</span>
    <span className="badge badge--success badge--notification">12</span>
    <span className="badge badge--warning badge--notification">99+</span>
  </div>
</div>

```html
<span class="badge badge--primary badge--notification">3</span>
<span class="badge badge--error badge--notification">9</span>
<span class="badge badge--success badge--notification">12</span>
<span class="badge badge--warning badge--notification">99+</span>
```

## Dot Badges

<div className="component-preview component-preview--center">
  <div className="badge-group">
    <span className="badge badge--success badge--dot"></span> <span style={{marginLeft: '0.5rem'}}>Online</span>
    <span className="badge badge--error badge--dot" style={{marginLeft: '2rem'}}></span> <span style={{marginLeft: '0.5rem'}}>Offline</span>
    <span className="badge badge--warning badge--dot" style={{marginLeft: '2rem'}}></span> <span style={{marginLeft: '0.5rem'}}>Away</span>
    <span className="badge badge--info badge--dot" style={{marginLeft: '2rem'}}></span> <span style={{marginLeft: '0.5rem'}}>Busy</span>
  </div>
</div>

```html
<span class="badge badge--success badge--dot"></span> <span>Online</span>
```

## Positioned Badges

<div className="component-preview component-preview--center">
  <div className="badge-group">
    <div className="badge-demo-container" style={{position: 'relative', display: 'inline-block'}}>
      <button className="button button--primary">Messages</button>
      <span className="badge badge--error badge--notification badge__positioned badge__positioned--top-right">5</span>
    </div>
    <div className="badge-demo-container" style={{position: 'relative', display: 'inline-block'}}>
      <button className="button button--primary">Notifications</button>
      <span className="badge badge--error badge--notification badge__positioned badge__positioned--top-left">12</span>
    </div>
  </div>
</div>

```html
<div
  class="badge-demo-container"
  style="position: relative; display: inline-block;"
>
  <button class="button button--primary">Messages</button>
  <span
    class="badge badge--error badge--notification badge__positioned badge__positioned--top-right"
    >5</span
  >
</div>
```

## Interactive Badges

### Clickable Badges

<div className="component-preview component-preview--center">
  <div className="badge-group">
    <span className="badge badge--primary badge--clickable">Click Me</span>
    <span className="badge badge--success badge--clickable">Interactive</span>
    <span className="badge badge--error badge--clickable">Action</span>
  </div>
</div>

```html
<span class="badge badge--primary badge--clickable">Click Me</span>
```

### Badges with Close Button

<div className="component-preview component-preview--center">
  <div className="badge-group">
    <span className="badge badge--primary">
      React
      <button className="badge__close" aria-label="Remove"></button>
    </span>
    <span className="badge badge--success">
      JavaScript
      <button className="badge__close" aria-label="Remove"></button>
    </span>
    <span className="badge badge--error">
      TypeScript
      <button className="badge__close" aria-label="Remove"></button>
    </span>
  </div>
</div>

```html
<span class="badge badge--primary">
  React
  <button class="badge__close" aria-label="Remove"></button>
</span>
```

## Badges with Icons

<div className="component-preview component-preview--center">
  <div className="badge-group">
    <span className="badge badge--primary">
      <span className="badge__icon">✓</span>
      Verified
    </span>
    <span className="badge badge--success">
      <span className="badge__icon">★</span>
      Featured
    </span>
    <span className="badge badge--error">
      <span className="badge__icon">✕</span>
      Denied
    </span>
    <span className="badge badge--warning">
      <span className="badge__icon">⚠</span>
      Warning
    </span>
  </div>
</div>

```html
<span class="badge badge--primary">
  <span class="badge__icon">✓</span>
  Verified
</span>
```

## Combined Styles

<div className="component-preview component-preview--center">
  <div className="badge-group">
    <span className="badge badge--outline badge--primary badge--pill">Outline + Pill</span>
    <span className="badge badge--soft badge--success badge--pill">Soft + Pill</span>
    <span className="badge badge--primary badge--lg badge--pill">Large + Pill</span>
  </div>
</div>

```html
<span class="badge badge--outline badge--primary badge--pill"
  >Outline + Pill</span
>
<span class="badge badge--soft badge--success badge--pill">Soft + Pill</span>
<span class="badge badge--primary badge--lg badge--pill">Large + Pill</span>
```

## Usage Guidelines

- **Primary**: Main actions, featured items
- **Secondary**: Secondary information, neutral states
- **Success**: Positive actions, confirmations, "New" items
- **Error**: Critical states, sales, urgent actions
- **Warning**: Caution states, trending items
- **Info**: Informational badges, help indicators
- **Notification**: Use for counters and numeric indicators
- **Dot**: Use for status indicators (online/offline)
- **Outline**: Use when you need less visual weight
- **Soft**: Use for subtle, non-intrusive labels

## Accessibility

- Badges should be used for visual enhancement only.
- Important information should also be available in text form.
- Use `aria-label` for close buttons.
- Ensure sufficient color contrast for readability.
- Don't rely solely on color to convey meaning.
