---
sidebar_label: "Modal"
---

# Modal Component

Display content in an overlay dialog that requires user interaction. Modals provide a focused state by blocking interactions with the rest of the page.

## 1. Basic Modal

Simple modal with header, body, and footer.

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
        <p>
          Click the close button, press ESC, or click outside the modal to close
          it.
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

| Modifier     | Description      | Max Width |
| :----------- | :--------------- | :-------- |
| `.modal--sm` | Small modal      | 400px     |
| `.modal--md` | Medium (Default) | 600px     |
| `.modal--lg` | Large modal      | 800px     |
| `.modal--xl` | Extra Large      | 1000px    |

```html
<!-- Trigger Buttons -->
<div class="demo-buttons">
  <button class="button button--primary" onclick="openModal('modal-sm')">
    Small Modal
  </button>
  <button class="button button--primary" onclick="openModal('modal-md')">
    Medium Modal
  </button>
  <button class="button button--primary" onclick="openModal('modal-lg')">
    Large Modal
  </button>
  <button class="button button--primary" onclick="openModal('modal-xl')">
    Extra Large Modal
  </button>
</div>

<!-- Small Modal -->
<div class="modal modal--sm" id="modal-sm">
  <div class="modal__backdrop" onclick="closeModal('modal-sm')"></div>
  <div class="modal__container">
    <div class="modal__dialog">
      <div class="modal__header">
        <h2 class="modal__title">Small Modal</h2>
        <button class="modal__close" onclick="closeModal('modal-sm')">×</button>
      </div>
      <div class="modal__body">
        <p>
          This is a small modal, perfect for simple confirmations or alerts.
        </p>
      </div>
      <div class="modal__footer">
        <button
          class="button button--sm button--secondary"
          onclick="closeModal('modal-sm')"
        >
          Close
        </button>
      </div>
    </div>
  </div>
</div>

<!-- Large Modal -->
<div class="modal modal--lg" id="modal-lg">
  <!-- Content -->
</div>
```

## 3. Scrollable Content Modal

When content exceeds the viewport height or the modal body height, the body area will scroll automatically while the header and footer remain fixed.

```html
<!-- Trigger Button -->
<button class="button button--primary" onclick="openModal('modal-scroll')">
  Open Scrollable Modal
</button>

<div class="modal" id="modal-scroll">
  <div class="modal__backdrop" onclick="closeModal('modal-scroll')"></div>
  <div class="modal__container">
    <div class="modal__dialog">
      <div class="modal__header">
        <h2 class="modal__title">Terms and Conditions</h2>
        <button class="modal__close" onclick="closeModal('modal-scroll')">
          ×
        </button>
      </div>
      <div class="modal__body">
        <!-- Long content here will scroll -->
        <h4>1. Introduction</h4>
        <p>Lorem ipsum dolor sit amet...</p>
        <!-- ... more content ... -->
      </div>
      <div class="modal__footer">
        <button
          class="button button--primary"
          onclick="closeModal('modal-scroll')"
        >
          Accept
        </button>
      </div>
    </div>
  </div>
</div>
```

## 4. Fullscreen Modal

Modal that takes up the entire viewport. Use the `.modal--fullscreen` modifier.

```html
<!-- Trigger Button -->
<button class="button button--primary" onclick="openModal('modal-fullscreen')">
  Open Fullscreen Modal
</button>

<div class="modal modal--fullscreen" id="modal-fullscreen">
  <div class="modal__backdrop" onclick="closeModal('modal-fullscreen')"></div>
  <div class="modal__container">
    <div class="modal__dialog">
      <div class="modal__header">
        <h2 class="modal__title">Fullscreen Modal</h2>
        <button class="modal__close" onclick="closeModal('modal-fullscreen')">
          ×
        </button>
      </div>
      <div class="modal__body">
        <p>
          This modal takes up the entire screen, perfect for immersive
          experiences.
        </p>
      </div>
      <div class="modal__footer">
        <button
          class="button button--secondary"
          onclick="closeModal('modal-fullscreen')"
        >
          Close
        </button>
      </div>
    </div>
  </div>
</div>
```

## 5. Animation Variants

Different animation styles for modal entrance can be applied using modifiers.

| Modifier             | Description                 |
| :------------------- | :-------------------------- |
| `.modal--fade`       | Simple fade in (no scaling) |
| `.modal--slide-down` | Slides down from top        |
| `.modal--slide-up`   | Slides up from bottom       |

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

<!-- Slide Up Modal -->
<div class="modal modal--slide-up" id="modal-slide-up">
  <div class="modal__backdrop" onclick="closeModal('modal-slide-up')"></div>
  <div class="modal__container">
    <div class="modal__dialog">
      <div class="modal__header">
        <h2 class="modal__title">Slide Up Animation</h2>
        <button class="modal__close" onclick="closeModal('modal-slide-up')">
          ×
        </button>
      </div>
      <div class="modal__body">
        <p>This modal slides up from the bottom of the screen.</p>
      </div>
    </div>
  </div>
</div>
```

## 6. Form in Modal

Modals are frequently used for forms. The structure supports form elements within the body.

```html
<!-- Trigger Button -->
<button class="button button--primary" onclick="openModal('modal-form')">
  Open Form Modal
</button>

<div class="modal" id="modal-form">
  <div class="modal__backdrop" onclick="closeModal('modal-form')"></div>
  <div class="modal__container">
    <div class="modal__dialog">
      <div class="modal__header">
        <h2 class="modal__title">Contact Us</h2>
        <button class="modal__close" onclick="closeModal('modal-form')">
          ×
        </button>
      </div>
      <div class="modal__body">
        <form>
          <div class="form-group">
            <label class="form-group__label" for="email">Email</label>
            <input
              type="email"
              id="email"
              class="input"
              placeholder="your@email.com"
              required
            />
          </div>
          <!-- More form fields -->
        </form>
      </div>
      <div class="modal__footer">
        <button
          class="button button--secondary"
          onclick="closeModal('modal-form')"
        >
          Cancel
        </button>
        <button
          class="button button--primary"
          onclick="closeModal('modal-form')"
        >
          Send Message
        </button>
      </div>
    </div>
  </div>
</div>
```

## 7. Confirmation Dialog

A small modal specifically styled for critical actions, often using different button variants (e.g., destructive actions).

```html
<!-- Trigger Button -->
<button class="button button--error" onclick="openModal('modal-confirm')">
  Delete Item
</button>

<div class="modal modal--sm" id="modal-confirm">
  <div class="modal__backdrop" onclick="closeModal('modal-confirm')"></div>
  <div class="modal__container">
    <div class="modal__dialog">
      <div class="modal__header">
        <h2 class="modal__title">Confirm Deletion</h2>
        <button class="modal__close" onclick="closeModal('modal-confirm')">
          ×
        </button>
      </div>
      <div class="modal__body">
        <p>
          Are you sure you want to delete this item? This action cannot be
          undone.
        </p>
      </div>
      <div class="modal__footer">
        <button
          class="button button--sm button--secondary"
          onclick="closeModal('modal-confirm')"
        >
          Cancel
        </button>
        <button
          class="button button--sm button--error"
          onclick="closeModal('modal-confirm')"
        >
          Delete
        </button>
      </div>
    </div>
  </div>
</div>
```

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

To make the modal functional (toggle visibility, handle accessibility, lock scroll), use the following JavaScript implementation:

```javascript
// Open modal function
function openModal(modalId) {
  const modal = document.getElementById(modalId);
  if (modal) {
    modal.classList.add("is-open");
    document.body.classList.add("modal-open");

    // Focus the close button for accessibility
    setTimeout(() => {
      const closeBtn = modal.querySelector(".modal__close");
      if (closeBtn) closeBtn.focus();
    }, 100);
  }
}

// Close modal function
function closeModal(modalId) {
  const modal = document.getElementById(modalId);
  if (modal) {
    modal.classList.remove("is-open");
    document.body.classList.remove("modal-open");
  }
}

// Close modal on ESC key
document.addEventListener("keydown", function (e) {
  if (e.key === "Escape") {
    const openModal = document.querySelector(".modal.is-open");
    if (openModal) {
      openModal.classList.remove("is-open");
      document.body.classList.remove("modal-open");
    }
  }
});
```
