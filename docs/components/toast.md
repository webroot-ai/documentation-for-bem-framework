---
sidebar_label: "Toast"
---

# Toast

Toasts are lightweight notifications designed to mimic the push notifications that have been popularized by mobile and desktop operating systems. They are temporary, non-critical notifications that appear in the corner of the screen.

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

Toast notifications come in four variants to communicate different types of messages:

<div className="component-preview component-preview--column">
  <div className="toast toast--info" style={{position: 'static'}}>
    <span className="toast__icon icon-info"></span>
    <div className="toast__content">
      <h4 className="toast__title">Information</h4>
      <p className="toast__description">This is an informational notification.</p>
    </div>
    <button className="toast__close" aria-label="Close notification">×</button>
  </div>

  <div className="toast toast--success" style={{position: 'static'}}>
    <span className="toast__icon icon-checkmark-circle"></span>
    <div className="toast__content">
      <h4 className="toast__title">Success!</h4>
      <p className="toast__description">Your action was completed successfully.</p>
    </div>
    <button className="toast__close" aria-label="Close notification">×</button>
  </div>

  <div className="toast toast--warning" style={{position: 'static'}}>
    <span className="toast__icon icon-notification"></span>
    <div className="toast__content">
      <h4 className="toast__title">Warning</h4>
      <p className="toast__description">Please review this carefully.</p>
    </div>
    <button className="toast__close" aria-label="Close notification">×</button>
  </div>

  <div className="toast toast--error" style={{position: 'static'}}>
    <span className="toast__icon icon-cancel-circle"></span>
    <div className="toast__content">
      <h4 className="toast__title">Error</h4>
      <p className="toast__description">Something went wrong.</p>
    </div>
    <button className="toast__close" aria-label="Close notification">×</button>
  </div>
</div>

```html
<!-- Info Toast -->
<div class="toast toast--info">
  <span class="toast__icon icon-info"></span>
  <div class="toast__content">
    <h4 class="toast__title">Information</h4>
    <p class="toast__description">This is an informational notification.</p>
  </div>
  <button class="toast__close" aria-label="Close notification">×</button>
</div>

<!-- Success Toast -->
<div class="toast toast--success">
  <span class="toast__icon icon-checkmark-circle"></span>
  <div class="toast__content">
    <h4 class="toast__title">Success!</h4>
    <p class="toast__description">Your action was completed successfully.</p>
  </div>
  <button class="toast__close" aria-label="Close notification">×</button>
</div>

<!-- Warning Toast -->
<div class="toast toast--warning">
  <span class="toast__icon icon-notification"></span>
  <div class="toast__content">
    <h4 class="toast__title">Warning</h4>
    <p class="toast__description">Please review this carefully.</p>
  </div>
  <button class="toast__close" aria-label="Close notification">×</button>
</div>

<!-- Error Toast -->
<div class="toast toast--error">
  <span class="toast__icon icon-cancel-circle"></span>
  <div class="toast__content">
    <h4 class="toast__title">Error</h4>
    <p class="toast__description">Something went wrong.</p>
  </div>
  <button class="toast__close" aria-label="Close notification">×</button>
</div>
```

## Positions

Toasts can be positioned in six different locations on the screen using position modifiers:

- `.toast--top-right` (default)
- `.toast--top-left`
- `.toast--top-center`
- `.toast--bottom-right`
- `.toast--bottom-left`
- `.toast--bottom-center`

```html
<!-- Top Right (default) -->
<div class="toast toast--top-right">...</div>

<!-- Top Left -->
<div class="toast toast--top-left">...</div>

<!-- Top Center -->
<div class="toast toast--top-center">...</div>

<!-- Bottom Right -->
<div class="toast toast--bottom-right">...</div>

<!-- Bottom Left -->
<div class="toast toast--bottom-left">...</div>

<!-- Bottom Center -->
<div class="toast toast--bottom-center">...</div>
```

## Toast Container

When displaying multiple toasts, wrap them in a `.toast-container` to handle stacking. The container should have a matching position modifier.

```html
<div class="toast-container toast-container--top-right">
  <div class="toast toast--success">...</div>
  <div class="toast toast--info">...</div>
  <div class="toast toast--warning">...</div>
</div>
```

## Toast with Progress Bar

Add a progress bar to visually indicate the time until auto-dismiss:

<div className="component-preview component-preview--center">
  <div className="toast toast--success" style={{position: 'static'}}>
    <span className="toast__icon icon-checkmark-circle"></span>
    <div className="toast__content">
      <h4 className="toast__title">Auto-Dismiss</h4>
      <p className="toast__description">This toast will auto-dismiss in 5 seconds.</p>
    </div>
    <button className="toast__close" aria-label="Close notification">×</button>
    <div className="toast__progress"></div>
  </div>
</div>

```html
<div class="toast toast--success">
  <span class="toast__icon icon-checkmark-circle"></span>
  <div class="toast__content">
    <h4 class="toast__title">Auto-Dismiss</h4>
    <p class="toast__description">This toast will auto-dismiss in 5 seconds.</p>
  </div>
  <button class="toast__close" aria-label="Close notification">×</button>
  <div class="toast__progress"></div>
</div>
```

## Sizes

Toasts are available in three sizes: small, default, and large.

### Small

<div className="component-preview component-preview--center">
  <div className="toast toast--sm toast--info" style={{position: 'static'}}>
    <span className="toast__icon icon-info"></span>
    <div className="toast__content">
      <h4 className="toast__title">Small Toast</h4>
      <p className="toast__description">This is a small sized toast notification.</p>
    </div>
    <button className="toast__close" aria-label="Close notification">×</button>
  </div>
</div>

```html
<div class="toast toast--sm">...</div>
```

### Default

<div className="component-preview component-preview--center">
  <div className="toast toast--info" style={{position: 'static'}}>
    <span className="toast__icon icon-info"></span>
    <div className="toast__content">
      <h4 className="toast__title">Default Toast</h4>
      <p className="toast__description">This is a default sized toast notification.</p>
    </div>
    <button className="toast__close" aria-label="Close notification">×</button>
  </div>
</div>

```html
<div class="toast">...</div>
```

### Large

<div className="component-preview component-preview--center">
  <div className="toast toast--lg toast--info" style={{position: 'static'}}>
    <span className="toast__icon icon-info"></span>
    <div className="toast__content">
      <h4 className="toast__title">Large Toast</h4>
      <p className="toast__description">This is a large sized toast notification.</p>
    </div>
    <button className="toast__close" aria-label="Close notification">×</button>
  </div>
</div>

```html
<div class="toast toast--lg">...</div>
```

## Usage Guidelines

### When to Use Toasts

- **Temporary notifications**: Use toasts for non-critical messages that don't require immediate action
- **Success confirmations**: Confirm that an action was completed successfully
- **Background updates**: Notify users of background processes or updates
- **Non-blocking messages**: Display information without interrupting the user's workflow

### Best Practices

- **Auto-dismiss**: Toasts should auto-dismiss after 5 seconds by default
- **Position consistency**: Position toasts consistently throughout your application (usually top-right or bottom-right)
- **Limit stacking**: Don't stack more than 3-4 toasts at once to avoid overwhelming users
- **Always closeable**: Always provide a close button for accessibility
- **Use containers**: Use the toast container for managing multiple toasts
- **Appropriate variants**: Choose the right variant (info, success, warning, error) for the message type
- **Clear messaging**: Keep messages concise and actionable

### Accessibility

- Include `role="alert"` and `aria-live="assertive"` for screen readers
- Provide descriptive `aria-label` attributes for close buttons
- Ensure sufficient color contrast for all variants
- Make sure toasts are keyboard accessible
- Don't rely solely on color to convey meaning; use icons and text

## Available Modifiers

### Variants

- `toast--info` - Informational messages
- `toast--success` - Success confirmations
- `toast--warning` - Warning messages
- `toast--error` - Error notifications

### Positions

- `toast--top-right` - Top right corner (default)
- `toast--top-left` - Top left corner
- `toast--top-center` - Top center
- `toast--bottom-right` - Bottom right corner
- `toast--bottom-left` - Bottom left corner
- `toast--bottom-center` - Bottom center

### Sizes

- `toast--sm` - Small toast
- Default (no modifier) - Standard size
- `toast--lg` - Large toast

### Elements

- `.toast__icon` - Icon container
- `.toast__content` - Content wrapper
- `.toast__title` - Toast title
- `.toast__description` - Toast message
- `.toast__close` - Close button
- `.toast__progress` - Progress bar for auto-dismiss
