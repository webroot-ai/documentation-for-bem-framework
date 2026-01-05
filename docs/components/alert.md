---
sidebar_label: "Alert"
---

# Alert

Alerts provide contextual feedback messages for typical user actions. They are available in multiple variants, styles, and layouts.

## Base Usage

The base `.alert` class provides a container for the alert content.

<div className="component-preview component-preview--center">
  <div className="alert" role="alert">
    <div className="alert__content">
      <h4 className="alert__title">Default Alert</h4>
      <p className="alert__description">This is a default alert message.</p>
    </div>
  </div>
</div>

```html
<div class="alert" role="alert">
  <div class="alert__content">
    <h4 class="alert__title">Default Alert</h4>
    <p class="alert__description">This is a default alert message.</p>
  </div>
</div>
```

## Variants

Alerts come in four semantic color variants: Info, Success, Warning, and Error.

<div className="component-preview component-preview--column">
  <div className="alert alert--info" role="alert">
    <div className="alert__content">
      <h4 className="alert__title">Info Alert</h4>
      <p className="alert__description">Useful information for the user.</p>
    </div>
  </div>
  <div className="alert alert--success" role="alert">
    <div className="alert__content">
      <h4 className="alert__title">Success Alert</h4>
      <p className="alert__description">Action completed successfully.</p>
    </div>
  </div>

  <div className="alert alert--warning" role="alert">
    <div className="alert__content">
      <h4 className="alert__title">Warning Alert</h4>
      <p className="alert__description">Please be careful with this action.</p>
    </div>
  </div>

  <div className="alert alert--error" role="alert">
    <div className="alert__content">
      <h4 className="alert__title">Error Alert</h4>
      <p className="alert__description">Something went wrong.</p>
    </div>
  </div>
</div>

```html
<div class="alert alert--info">...</div>
<div class="alert alert--success">...</div>
<div class="alert alert--warning">...</div>
<div class="alert alert--error">...</div>
```

## Styles

### Solid

Solid alerts use a filled background color for higher contrast.

<div className="component-preview component-preview--column">
  <div className="alert alert--info alert--solid">
    <div className="alert__content">
      <h4 className="alert__title">Solid Info</h4>
      <p className="alert__description">A solid background style.</p>
    </div>
  </div>
</div>

```html
<div class="alert alert--info alert--solid">...</div>
```

### Bordered

Bordered alerts have a transparent background with a stronger border.

<div className="component-preview component-preview--column">
  <div className="alert alert--success alert--bordered">
    <div className="alert__content">
      <h4 className="alert__title">Bordered Success</h4>
      <p className="alert__description">A bordered style with transparent background.</p>
    </div>
  </div>
</div>

```html
<div class="alert alert--success alert--bordered">...</div>
```

### Accent

Accent alerts feature a thick left border for emphasis.

<div className="component-preview component-preview--column">
  <div className="alert alert--warning alert--accent">
    <div className="alert__content">
      <h4 className="alert__title">Accent Warning</h4>
      <p className="alert__description">An accented style with a left border.</p>
    </div>
  </div>
</div>

```html
<div class="alert alert--warning alert--accent">...</div>
```

## Layouts

### With Icon

Add an icon to the alert using the `.alert__icon` element and the `.alert--with-icon` modifier.

<div className="component-preview component-preview--column">
  <div className="alert alert--info alert--with-icon">
    <div className="alert__icon">ℹ️</div>
    <div className="alert__content">
      <h4 className="alert__title">With Icon</h4>
      <p className="alert__description">Alert with an icon for better recognition.</p>
    </div>
  </div>
</div>

```html
<div class="alert alert--info alert--with-icon">
  <div class="alert__icon">ℹ️</div>
  <div class="alert__content">...</div>
</div>
```

### Dismissible

Add a close button using the `.alert__close` element and the `.alert--dismissible` modifier.

<div className="component-preview component-preview--column">
  <div className="alert alert--success alert--dismissible">
    <div className="alert__content">
      <h4 className="alert__title">Dismissible</h4>
      <p className="alert__description">This alert can be closed.</p>
    </div>
    <button className="alert__close" aria-label="Close alert">×</button>
  </div>
</div>

```html
<div class="alert alert--success alert--dismissible">
  <div class="alert__content">...</div>
  <button class="alert__close" aria-label="Close alert">×</button>
</div>
```

### Inline

Inline alerts are more compact and lack a bottom margin.

<div className="component-preview component-preview--center">
  <div className="alert alert--error alert--inline alert--with-icon">
     <div className="alert__icon">⚠️</div>
    <div className="alert__content">
      <span className="alert__description">An inline error message.</span>
    </div>
  </div>
</div>

```html
<div class="alert alert--error alert--inline alert--with-icon">
  <div class="alert__icon">⚠️</div>
  <div class="alert__content">
    <span class="alert__description">An inline error message.</span>
  </div>
</div>
```

## Sizes

### Small

<div className="component-preview component-preview--column">
  <div className="alert alert--info alert--sm">
    <div className="alert__content">
      <h4 className="alert__title">Small Alert</h4>
      <p className="alert__description">Compact version.</p>
    </div>
  </div>
</div>

```html
<div class="alert alert--info alert--sm">...</div>
```

### Large

<div className="component-preview component-preview--column">
  <div className="alert alert--info alert--lg">
    <div className="alert__content">
      <h4 className="alert__title">Large Alert</h4>
      <p className="alert__description">Prominent version with larger text/padding.</p>
    </div>
  </div>
</div>

```html
<div class="alert alert--info alert--lg">...</div>
```
