---
sidebar_label: "Modal"
---

export const openModal = (id) => {
  if (typeof document !== 'undefined') {
    const modal = document.getElementById(id);
    if (modal) {
      modal.classList.add('is-open');
      document.body.classList.add('modal-open');
    }
  }
};

export const closeModal = (id) => {
  if (typeof document !== 'undefined') {
    const modal = document.getElementById(id);
    if (modal) {
      modal.classList.remove('is-open');
      document.body.classList.remove('modal-open');
    }
  }
};

# Modal Component

Display content in an overlay dialog that requires user interaction. Modals provide a focused state by blocking interactions with the rest of the page.

## 1. Basic Modal

Simple modal with header, body, and footer.

<div className="component-preview component-preview--center">
  <button className="button button--primary" onClick={() => openModal('modal-basic-demo')}>
    Open Basic Modal
  </button>
</div>

{/* Rendered Modal for Demo */}
<div className="modal" id="modal-basic-demo">
  <div className="modal__backdrop" onClick={() => closeModal('modal-basic-demo')}></div>
  <div className="modal__container" onClick={(e) => e.target === e.currentTarget && closeModal('modal-basic-demo')}>
    <div className="modal__dialog">
      <div className="modal__header">
        <h2 className="modal__title">Basic Modal</h2>
        <button className="modal__close" onClick={() => closeModal('modal-basic-demo')} aria-label="Close modal">×</button>
      </div>
      <div className="modal__body">
        <p>This is the basic modal demo. You can close it by clicking the backdrop, the X, or the close button below.</p>
      </div>
      <div className="modal__footer">
        <button className="button button--secondary" onClick={() => closeModal('modal-basic-demo')}>Close</button>
      </div>
    </div>
  </div>
</div>

```html
<!-- Trigger Button -->
<button class="button button--primary" onclick="openModal('modal-basic')">
  Open Basic Modal
</button>

<!-- Modal Structure -->
<div class="modal" id="modal-basic">
  <div class="modal__backdrop" onclick="closeModal('modal-basic')"></div>
  <div class="modal__container">
    <div class="modal__dialog">
      <div class="modal__header">
        <h2 class="modal__title">Modal Title</h2>
        <button
          class="modal__close"
          onclick="closeModal('modal-basic')"
          aria-label="Close modal"
        >
          ×
        </button>
      </div>
      <div class="modal__body">
        <p>
          This is a basic modal dialog. You can put any content here. The modal
          will center itself on the screen and show a backdrop behind it.
        </p>
      </div>
      <div class="modal__footer">
        <button
          class="button button--secondary"
          onclick="closeModal('modal-basic')"
        >
          Cancel
        </button>
        <button
          class="button button--primary"
          onclick="closeModal('modal-basic')"
        >
          Confirm
        </button>
      </div>
    </div>
  </div>
</div>
```

## 2. Modal Sizes

Different modal sizes for various use cases. Use the modifier classes on the `.modal` container.

| Modifier | Description | Max Width |
| :--- | :--- | :--- |
| `.modal--sm` | Small modal | 400px |
| `.modal--md` | Medium (Default) | 600px |
| `.modal--lg` | Large modal | 800px |
| `.modal--xl` | Extra Large | 1000px |

<div className="component-preview component-preview--center">
  <div className="demo-buttons">
    <button className="button button--primary" onClick={() => openModal('modal-sm-demo')}>Small</button>
    <button className="button button--primary" onClick={() => openModal('modal-md-demo')}>Medium</button>
    <button className="button button--primary" onClick={() => openModal('modal-lg-demo')}>Large</button>
    <button className="button button--primary" onClick={() => openModal('modal-xl-demo')}>X-Large</button>
  </div>
</div>

```html
<!-- Example of a Small Modal -->
<div class="modal modal--sm" id="modal-small">
  <div class="modal__backdrop" onclick="closeModal('modal-small')"></div>
  <div class="modal__container">
    <div class="modal__dialog">
      <div class="modal__header">
        <h2 class="modal__title">Small Modal</h2>
        <button class="modal__close" onclick="closeModal('modal-small')">×</button>
      </div>
      <div class="modal__body">
        <p>This is a small sized modal.</p>
      </div>
    </div>
  </div>
</div>
```

{/* Rendered Modals for Demo */}
<div className="modal modal--sm" id="modal-sm-demo">
  <div className="modal__backdrop" onClick={() => closeModal('modal-sm-demo')}></div>
  <div className="modal__container" onClick={(e) => e.target === e.currentTarget && closeModal('modal-sm-demo')}>
    <div className="modal__dialog">
      <div className="modal__header"><h2 className="modal__title">Small Modal</h2><button className="modal__close" onClick={() => closeModal('modal-sm-demo')}>×</button></div>
      <div className="modal__body"><p>This is a small modal.</p></div>
    </div>
  </div>
</div>

<div className="modal modal--md" id="modal-md-demo">
  <div className="modal__backdrop" onClick={() => closeModal('modal-md-demo')}></div>
  <div className="modal__container" onClick={(e) => e.target === e.currentTarget && closeModal('modal-md-demo')}>
    <div className="modal__dialog">
      <div className="modal__header"><h2 className="modal__title">Medium Modal</h2><button className="modal__close" onClick={() => closeModal('modal-md-demo')}>×</button></div>
      <div className="modal__body"><p>This is a medium modal (default).</p></div>
    </div>
  </div>
</div>

<div className="modal modal--lg" id="modal-lg-demo">
  <div className="modal__backdrop" onClick={() => closeModal('modal-lg-demo')}></div>
  <div className="modal__container" onClick={(e) => e.target === e.currentTarget && closeModal('modal-lg-demo')}>
    <div className="modal__dialog">
      <div className="modal__header"><h2 className="modal__title">Large Modal</h2><button className="modal__close" onClick={() => closeModal('modal-lg-demo')}>×</button></div>
      <div className="modal__body"><p>This is a large modal.</p></div>
    </div>
  </div>
</div>

<div className="modal modal--xl" id="modal-xl-demo">
  <div className="modal__backdrop" onClick={() => closeModal('modal-xl-demo')}></div>
  <div className="modal__container" onClick={(e) => e.target === e.currentTarget && closeModal('modal-xl-demo')}>
    <div className="modal__dialog">
      <div className="modal__header"><h2 className="modal__title">Extra Large Modal</h2><button className="modal__close" onClick={() => closeModal('modal-xl-demo')}>×</button></div>
      <div className="modal__body"><p>This is an extra large modal.</p></div>
    </div>
  </div>
</div>

## 3. Scrollable Content Modal

When content exceeds the viewport height or the modal body height, the body area will scroll automatically while the header and footer remain fixed.

<div className="component-preview component-preview--center">
  <button className="button button--primary" onClick={() => openModal('modal-scroll-demo')}>
    Open Scrollable Modal
  </button>
</div>

```html
<!-- Trigger Button -->
<button class="button button--primary" onclick="openModal('modal-scroll')">
  Open Scrollable Modal
</button>

<div class="modal" id="modal-scroll">
  ...
</div>
```

{/* Rendered Modal for Demo */}
<div className="modal" id="modal-scroll-demo">
  <div className="modal__backdrop" onClick={() => closeModal('modal-scroll-demo')}></div>
  <div className="modal__container" onClick={(e) => e.target === e.currentTarget && closeModal('modal-scroll-demo')}>
    <div className="modal__dialog">
      <div className="modal__header">
        <h2 className="modal__title">Terms and Conditions</h2>
        <button className="modal__close" onClick={() => closeModal('modal-scroll-demo')}>×</button>
      </div>
      <div className="modal__body" style={{maxHeight: '300px', overflowY: 'auto'}}>
        <h4>1. Introduction</h4>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
        <p>Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</p>
        <p>Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.</p>
        <p>Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
        <p>Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam.</p>
      </div>
      <div className="modal__footer">
        <button className="button button--primary" onClick={() => closeModal('modal-scroll-demo')}>Accept</button>
      </div>
    </div>
  </div>
</div>

## 4. Fullscreen Modal

Modal that takes up the entire viewport. Use the `.modal--fullscreen` modifier.

<div className="component-preview component-preview--center">
  <button className="button button--primary" onClick={() => openModal('modal-fullscreen-demo')}>
    Open Fullscreen Modal
  </button>
</div>

```html
<!-- Trigger Button -->
<button class="button button--primary" onclick="openModal('modal-fullscreen')">
  Open Fullscreen Modal
</button>

<div class="modal modal--fullscreen" id="modal-fullscreen">
  ...
</div>
```

{/* Rendered Modal for Demo */}
<div className="modal modal--fullscreen" id="modal-fullscreen-demo">
  <div className="modal__backdrop" onClick={() => closeModal('modal-fullscreen-demo')}></div>
  <div className="modal__container" onClick={(e) => e.target === e.currentTarget && closeModal('modal-fullscreen-demo')}>
    <div className="modal__dialog">
      <div className="modal__header">
        <h2 className="modal__title">Fullscreen Modal</h2>
        <button className="modal__close" onClick={() => closeModal('modal-fullscreen-demo')}>×</button>
      </div>
      <div className="modal__body">
        <p>This modal takes up the entire screen, perfect for immersive experiences.</p>
      </div>
      <div className="modal__footer">
        <button className="button button--secondary" onClick={() => closeModal('modal-fullscreen-demo')}>Close</button>
      </div>
    </div>
  </div>
</div>

## 5. Animation Variants

Different animation styles for modal entrance can be applied using modifiers.

| Modifier             | Description                 |
| :------------------- | :-------------------------- |
| `.modal--fade`       | Simple fade in (no scaling) |
| `.modal--slide-down` | Slides down from top        |
| `.modal--slide-up`   | Slides up from bottom       |

<div className="component-preview component-preview--center">
  <div className="demo-buttons">
    <button className="button button--primary" onClick={() => openModal('modal-fade-demo')}>
      Fade Animation
    </button>
    <button className="button button--primary" onClick={() => openModal('modal-slide-down-demo')}>
      Slide Down
    </button>
    <button className="button button--primary" onClick={() => openModal('modal-slide-up-demo')}>
      Slide Up
    </button>
  </div>
</div>

```html
<!-- Trigger Buttons -->
<div class="demo-buttons">
  <button class="button button--primary" onclick="openModal('modal-fade')">
    Fade Animation
  </button>
  <button
    class="button button--primary"
    onclick="openModal('modal-slide-down')"
  >
    Slide Down
  </button>
  <button class="button button--primary" onclick="openModal('modal-slide-up')">
    Slide Up
  </button>
</div>
```

{/* Rendered Modals for Demo */}
<div className="modal modal--fade" id="modal-fade-demo">
  <div className="modal__backdrop" onClick={() => closeModal('modal-fade-demo')}></div>
  <div className="modal__container" onClick={(e) => e.target === e.currentTarget && closeModal('modal-fade-demo')}>
    <div className="modal__dialog">
      <div className="modal__header"><h2 className="modal__title">Fade Animation</h2><button className="modal__close" onClick={() => closeModal('modal-fade-demo')}>×</button></div>
      <div className="modal__body"><p>This modal fades in.</p></div>
    </div>
  </div>
</div>

<div className="modal modal--slide-down" id="modal-slide-down-demo">
  <div className="modal__backdrop" onClick={() => closeModal('modal-slide-down-demo')}></div>
  <div className="modal__container" onClick={(e) => e.target === e.currentTarget && closeModal('modal-slide-down-demo')}>
    <div className="modal__dialog">
      <div className="modal__header"><h2 className="modal__title">Slide Down</h2><button className="modal__close" onClick={() => closeModal('modal-slide-down-demo')}>×</button></div>
      <div className="modal__body"><p>This modal slides down from the top.</p></div>
    </div>
  </div>
</div>

<div className="modal modal--slide-up" id="modal-slide-up-demo">
  <div className="modal__backdrop" onClick={() => closeModal('modal-slide-up-demo')}></div>
  <div className="modal__container" onClick={(e) => e.target === e.currentTarget && closeModal('modal-slide-up-demo')}>
    <div className="modal__dialog">
      <div className="modal__header"><h2 className="modal__title">Slide Up</h2><button className="modal__close" onClick={() => closeModal('modal-slide-up-demo')}>×</button></div>
      <div className="modal__body"><p>This modal slides up from the bottom.</p></div>
    </div>
  </div>
</div>

## 6. Form in Modal

Modals are frequently used for forms. The structure supports form elements within the body.

<div className="component-preview component-preview--center">
  <button className="button button--primary" onClick={() => openModal('modal-form-demo')}>
    Open Form Modal
  </button>
</div>

```html
<!-- Trigger Button -->
<button class="button button--primary" onclick="openModal('modal-form')">
  Open Form Modal
</button>

<div class="modal" id="modal-form">
  ...
</div>
```

{/* Rendered Modal for Demo */}
<div className="modal" id="modal-form-demo">
  <div className="modal__backdrop" onClick={() => closeModal('modal-form-demo')}></div>
  <div className="modal__container" onClick={(e) => e.target === e.currentTarget && closeModal('modal-form-demo')}>
    <div className="modal__dialog">
      <div className="modal__header">
        <h2 className="modal__title">Contact Us</h2>
        <button className="modal__close" onClick={() => closeModal('modal-form-demo')}>×</button>
      </div>
      <div className="modal__body">
        <form onSubmit={(e) => e.preventDefault()}>
          <div className="form-group">
            <label className="form-group__label" htmlFor="email-demo">Email</label>
            <input type="email" id="email-demo" className="input" placeholder="your@email.com" />
          </div>
        </form>
      </div>
      <div className="modal__footer">
        <button className="button button--secondary" onClick={() => closeModal('modal-form-demo')}>Cancel</button>
        <button className="button button--primary" onClick={() => closeModal('modal-form-demo')}>Send</button>
      </div>
    </div>
  </div>
</div>

## 7. Confirmation Dialog

A small modal specifically styled for critical actions, often using different button variants (e.g., destructive actions).

<div className="component-preview component-preview--center">
  <button className="button button--error" onClick={() => openModal('modal-confirm-demo')}>
    Delete Item
  </button>
</div>

```html
<!-- Trigger Button -->
<button class="button button--error" onclick="openModal('modal-confirm')">
  Delete Item
</button>

<div class="modal modal--sm" id="modal-confirm">
  ...
</div>
```

{/* Rendered Modal for Demo */}
<div className="modal modal--sm" id="modal-confirm-demo">
  <div className="modal__backdrop" onClick={() => closeModal('modal-confirm-demo')}></div>
  <div className="modal__container" onClick={(e) => e.target === e.currentTarget && closeModal('modal-confirm-demo')}>
    <div className="modal__dialog">
      <div className="modal__header">
        <h2 className="modal__title">Confirm Deletion</h2>
        <button className="modal__close" onClick={() => closeModal('modal-confirm-demo')}>×</button>
      </div>
      <div className="modal__body">
        <p>Are you sure you want to delete this item?</p>
      </div>
      <div className="modal__footer">
        <button className="button button--sm button--secondary" onClick={() => closeModal('modal-confirm-demo')}>Cancel</button>
        <button className="button button--sm button--error" onClick={() => closeModal('modal-confirm-demo')}>Delete</button>
      </div>
    </div>
  </div>
</div>

## Usage Notes

### Accessibility

- Always provide a close button with proper ARIA label.
- Use `role="dialog"` and `aria-modal="true"` on the modal dialog.
- Implement keyboard navigation (ESC to close, TAB to cycle through focusable elements).
- Trap focus within the modal when open.
- Return focus to the trigger element when closed.
- Prevent body scroll when modal is open.

### Available Modifiers

- **Sizes**: `--sm`, `--md`, `--lg`, `--xl`, `--fullscreen`
- **Animations**: `--fade`, `--slide-down`, `--slide-up`
- **Alignment**: `--top`, `--center`
- **Layout**: `--no-padding`

### JavaScript Integration

The modal component uses the `Modal` class for initialization and management. You can trigger modals using data attributes or programmatically.

#### Trigger using Data Attributes

Add `data-modal-trigger="MODAL_ID"` to any button to automatically open the corresponding modal.

```html
<button class="button button--primary" data-modal-trigger="modal-basic">
  Open Modal
</button>
```

#### Class Implementation

```javascript
import { Modal } from './components/modal.js';

// Initialize all modals on the page
Modal.initAll();

// Or initialize a specific modal
const modalElement = document.getElementById('modal-basic');
const modal = new Modal(modalElement);

// Programmatic control
modal.open();
modal.close();
if (modal.isOpen()) {
  console.log('Modal is open');
}
```


