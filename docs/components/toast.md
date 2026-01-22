---
sidebar_label: "Toast"
---

export const showToast = (type) => {
  if (typeof document !== 'undefined') {
    const container = document.querySelector('.toast-container--top-right') || createContainer('top-right');
    const toast = document.createElement('div');
    toast.className = `toast toast--${type}`;
    toast.innerHTML = `
      <span class="toast__icon"><i class="icon-info"></i></span>
      <div class="toast__content">
        <h4 class="toast__title">${type.charAt(0).toUpperCase() + type.slice(1)}</h4>
        <p class="toast__description">This is a ${type} notification.</p>
      </div>
      <button class="toast__close" aria-label="Close notification">×</button>
    `;
    container.appendChild(toast);
    setTimeout(() => toast.remove(), 5000);
    toast.querySelector('.toast__close').onclick = () => toast.remove();
  }
};

export const showToastPosition = (position) => {
  if (typeof document !== 'undefined') {
    const container = document.querySelector(`.toast-container--${position}`) || createContainer(position);
    const toast = document.createElement('div');
    toast.className = 'toast toast--info';
    toast.innerHTML = `
      <div class="toast__content">
        <h4 class="toast__title">Position: ${position}</h4>
        <p class="toast__description">Toast in ${position} corner.</p>
      </div>
    `;
    container.appendChild(toast);
    setTimeout(() => toast.remove(), 3000);
  }
};

export const showToastWithProgress = () => {
  if (typeof document !== 'undefined') {
    const container = document.querySelector('.toast-container--top-right') || createContainer('top-right');
    const toast = document.createElement('div');
    toast.className = 'toast toast--success';
    toast.innerHTML = `
      <div class="toast__content">
        <h4 class="toast__title">Progress Bar</h4>
        <p class="toast__description">Auto-dismissing in 5s...</p>
      </div>
      <div class="toast__progress" style="animation: toast-progress 5s linear forwards"></div>
    `;
    container.appendChild(toast);
    setTimeout(() => toast.remove(), 5000);
  }
};

export const showToastSize = (size) => {
  if (typeof document !== 'undefined') {
    const container = document.querySelector('.toast-container--top-right') || createContainer('top-right');
    const toast = document.createElement('div');
    toast.className = `toast toast--${size} toast--info`;
    toast.innerHTML = `
      <div class="toast__content">
        <h4 class="toast__title">${size === 'default' ? 'Default' : size.toUpperCase()} Size</h4>
        <p class="toast__description">This is a ${size} toast.</p>
      </div>
    `;
    container.appendChild(toast);
    setTimeout(() => toast.remove(), 3000);
  }
};

export const createContainer = (position) => {
  if (typeof document !== 'undefined') {
    const container = document.createElement('div');
    container.className = `toast-container toast-container--${position}`;
    document.body.appendChild(container);
    return container;
  }
};

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

<div className="component-preview component-preview--center">
  <div className="demo-buttons">
    <button className="button button--primary" onClick={() => showToast('info')}>Show Info Toast</button>
    <button className="button button--success" onClick={() => showToast('success')}>Show Success Toast</button>
    <button className="button button--warning" onClick={() => showToast('warning')}>Show Warning Toast</button>
    <button className="button button--danger" onClick={() => showToast('error')}>Show Error Toast</button>
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

<div className="component-preview component-preview--center">
  <div className="demo-buttons">
    <button className="button button--primary" onClick={() => showToastPosition('top-right')}>Top Right</button>
    <button className="button button--primary" onClick={() => showToastPosition('top-left')}>Top Left</button>
    <button className="button button--primary" onClick={() => showToastPosition('top-center')}>Top Center</button>
    <button className="button button--primary" onClick={() => showToastPosition('bottom-right')}>Bottom Right</button>
    <button className="button button--primary" onClick={() => showToastPosition('bottom-left')}>Bottom Left</button>
    <button className="button button--primary" onClick={() => showToastPosition('bottom-center')}>Bottom Center</button>
  </div>
</div>

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

<div className="component-preview component-preview--center">
  <button className="button button--primary" onClick={() => showToastWithProgress()}>
    Show Toast with Progress
  </button>
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

<div className="component-preview component-preview--center">
  <button className="button button--primary" onClick={() => showToastSize('sm')}>Small Toast</button>
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

<div className="component-preview component-preview--center">
  <button className="button button--primary" onClick={() => showToastSize('default')}>Default Toast</button>
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

<div className="component-preview component-preview--center">
  <button className="button button--primary" onClick={() => showToastSize('lg')}>Large Toast</button>
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

## Inline Alerts

Compact alerts that can be placed inline with content.

```html
<div class="alert alert--success alert--inline alert--with-icon">
  <span class="alert__icon icon-checkmark"></span>
  <div class="alert__content">Saved!</div>
</div>
```

## JavaScript Integration

The toast component can be managed using the `Toast` class.

### Class Implementation

```javascript
import { Toast } from './components/toast.js';

// Initialize any existing toasts
Toast.initAll();

// Show a toast programmatically
Toast.show({
  message: 'Your profile has been updated.',
  type: 'success',
  duration: 5000,
  position: 'top-right'
});

// Shorthand methods
Toast.success('Saved successfully!');
Toast.error('An error occurred.');
Toast.warning('Check your input.');
Toast.info('New message received.');
```

### Options

| Option     | Type     | Default      | Description                                     |
| :--------- | :------- | :----------- | :---------------------------------------------- |
| `message`  | `string` | -            | The message to display                          |
| `type`     | `string` | `'info'`     | `success`, `error`, `warning`, `info`           |
| `duration` | `number` | `5000`       | Time in ms before auto-dismiss (0 to disable)   |
| `position` | `string` | `'top-right'`| `top-right`, `top-left`, `bottom-right`, etc. |

