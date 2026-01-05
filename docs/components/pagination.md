---
sidebar_label: "Pagination"
---

# Pagination

Navigate through multiple pages of content with accessible pagination controls.

## Basic Pagination

Standard pagination with previous/next controls and numbered pages.

<div className="component-preview component-preview--center">
  <nav className="pagination" aria-label="Pagination">
    <ul className="pagination__list">
      <li className="pagination__item pagination__prev">
        <a href="#" className="pagination__link is-disabled" aria-label="Previous page">
          <span aria-hidden="true">←</span>
          <span>Previous</span>
        </a>
      </li>
      <li className="pagination__item">
        <a href="#" className="pagination__link is-active" aria-label="Page 1" aria-current="page">1</a>
      </li>
      <li className="pagination__item">
        <a href="#" className="pagination__link" aria-label="Page 2">2</a>
      </li>
      <li className="pagination__item">
        <a href="#" className="pagination__link" aria-label="Page 3">3</a>
      </li>
      <li className="pagination__item">
        <a href="#" className="pagination__link" aria-label="Page 4">4</a>
      </li>
      <li className="pagination__item">
        <a href="#" className="pagination__link" aria-label="Page 5">5</a>
      </li>
      <li className="pagination__item pagination__next">
        <a href="#" className="pagination__link" aria-label="Next page">
          <span>Next</span>
          <span aria-hidden="true">→</span>
        </a>
      </li>
    </ul>
  </nav>
</div>

```html
<nav class="pagination" aria-label="Pagination">
  <ul class="pagination__list">
    <li class="pagination__item pagination__prev">
      <a
        href="#"
        class="pagination__link is-disabled"
        aria-label="Previous page"
      >
        <span aria-hidden="true">←</span>
        <span>Previous</span>
      </a>
    </li>
    <li class="pagination__item">
      <a
        href="#"
        class="pagination__link is-active"
        aria-label="Page 1"
        aria-current="page"
        >1</a
      >
    </li>
    <!-- ... -->
    <li class="pagination__item pagination__next">
      <a href="#" class="pagination__link" aria-label="Next page">
        <span>Next</span>
        <span aria-hidden="true">→</span>
      </a>
    </li>
  </ul>
</nav>
```

## Pagination with Ellipsis

Shows truncated pages for large datasets.

<div className="component-preview component-preview--center">
  <nav className="pagination" aria-label="Pagination">
    <ul className="pagination__list">
      <li className="pagination__item pagination__prev">
        <a href="#" className="pagination__link" aria-label="Previous page">
          <span aria-hidden="true">←</span>
          <span>Prev</span>
        </a>
      </li>
      <li className="pagination__item">
        <a href="#" className="pagination__link" aria-label="Page 1">1</a>
      </li>
      <li className="pagination__item">
        <span className="pagination__ellipsis" aria-hidden="true">...</span>
      </li>
      <li className="pagination__item">
        <a href="#" className="pagination__link" aria-label="Page 5">5</a>
      </li>
      <li className="pagination__item">
        <a href="#" className="pagination__link is-active" aria-label="Page 6" aria-current="page">6</a>
      </li>
      <li className="pagination__item">
        <a href="#" className="pagination__link" aria-label="Page 7">7</a>
      </li>
      <li className="pagination__item">
        <span className="pagination__ellipsis" aria-hidden="true">...</span>
      </li>
      <li className="pagination__item">
        <a href="#" className="pagination__link" aria-label="Page 20">20</a>
      </li>
      <li className="pagination__item pagination__next">
        <a href="#" className="pagination__link" aria-label="Next page">
          <span>Next</span>
          <span aria-hidden="true">→</span>
        </a>
      </li>
    </ul>
  </nav>
</div>

```html
<li class="pagination__item">
  <span class="pagination__ellipsis" aria-hidden="true">...</span>
</li>
```

## Sizes

### Small Pagination

Compact size for tight spaces or mobile interfaces.

<div className="component-preview component-preview--center">
  <nav className="pagination pagination--sm" aria-label="Pagination">
    <ul className="pagination__list">
      <li className="pagination__item pagination__prev">
        <a href="#" className="pagination__link" aria-label="Previous page">
          <span aria-hidden="true">←</span>
        </a>
      </li>
      <li className="pagination__item">
        <a href="#" className="pagination__link" aria-label="Page 1">1</a>
      </li>
      <li className="pagination__item">
        <a href="#" className="pagination__link is-active" aria-label="Page 2" aria-current="page">2</a>
      </li>
      <li className="pagination__item">
        <a href="#" className="pagination__link" aria-label="Page 3">3</a>
      </li>
      <li className="pagination__item pagination__next">
        <a href="#" className="pagination__link" aria-label="Next page">
          <span aria-hidden="true">→</span>
        </a>
      </li>
    </ul>
  </nav>
</div>

```html
<nav class="pagination pagination--sm" aria-label="Pagination">...</nav>
```

### Large Pagination

Spacious size with increased touch targets for better usability.

<div className="component-preview component-preview--center">
  <nav className="pagination pagination--lg" aria-label="Pagination">
    <ul className="pagination__list">
      <li className="pagination__item pagination__prev">
        <a href="#" className="pagination__link" aria-label="Previous page">
          <span aria-hidden="true">←</span>
          <span>Previous</span>
        </a>
      </li>
      <li className="pagination__item">
        <a href="#" className="pagination__link" aria-label="Page 1">1</a>
      </li>
      <li className="pagination__item">
        <a href="#" className="pagination__link" aria-label="Page 2">2</a>
      </li>
      <li className="pagination__item">
        <a href="#" className="pagination__link is-active" aria-label="Page 3" aria-current="page">3</a>
      </li>
      <li className="pagination__item pagination__next">
        <a href="#" className="pagination__link" aria-label="Next page">
          <span>Next</span>
          <span aria-hidden="true">→</span>
        </a>
      </li>
    </ul>
  </nav>
</div>

```html
<nav class="pagination pagination--lg" aria-label="Pagination">...</nav>
```

## Styles

### Rounded Pagination

Fully rounded button style for a softer appearance.

<div className="component-preview component-preview--center">
  <nav className="pagination pagination--rounded" aria-label="Pagination">
    <ul className="pagination__list">
      <li className="pagination__item pagination__prev">
        <a href="#" className="pagination__link" aria-label="Previous page">
          <span aria-hidden="true">←</span>
        </a>
      </li>
      <li className="pagination__item">
        <a href="#" className="pagination__link" aria-label="Page 1">1</a>
      </li>
      <li className="pagination__item">
        <a href="#" className="pagination__link" aria-label="Page 2">2</a>
      </li>
      <li className="pagination__item">
        <a href="#" className="pagination__link is-active" aria-label="Page 3" aria-current="page">3</a>
      </li>
      <li className="pagination__item pagination__next">
        <a href="#" className="pagination__link" aria-label="Next page">
          <span aria-hidden="true">→</span>
        </a>
      </li>
    </ul>
  </nav>
</div>

```html
<nav class="pagination pagination--rounded" aria-label="Pagination">...</nav>
```

### Simple Pagination

Minimal style without borders, cleaner appearance.

<div className="component-preview component-preview--center">
  <nav className="pagination pagination--simple" aria-label="Pagination">
    <ul className="pagination__list">
      <li className="pagination__item pagination__prev">
        <a href="#" className="pagination__link" aria-label="Previous page">
          <span aria-hidden="true">←</span>
          <span>Previous</span>
        </a>
      </li>
      <li className="pagination__item">
        <a href="#" className="pagination__link" aria-label="Page 1">1</a>
      </li>
      <li className="pagination__item">
        <a href="#" className="pagination__link" aria-label="Page 2">2</a>
      </li>
      <li className="pagination__item">
        <a href="#" className="pagination__link is-active" aria-label="Page 3" aria-current="page">3</a>
      </li>
      <li className="pagination__item pagination__next">
        <a href="#" className="pagination__link" aria-label="Next page">
          <span>Next</span>
          <span aria-hidden="true">→</span>
        </a>
      </li>
    </ul>
  </nav>
</div>

```html
<nav class="pagination pagination--simple" aria-label="Pagination">...</nav>
```

### Outlined Pagination

Border-only style with transparent background.

<div className="component-preview component-preview--center">
  <nav className="pagination pagination--outlined" aria-label="Pagination">
    <ul className="pagination__list">
      <li className="pagination__item pagination__prev">
        <a href="#" className="pagination__link" aria-label="Previous page">
          <span aria-hidden="true">←</span>
        </a>
      </li>
      <li className="pagination__item">
        <a href="#" className="pagination__link" aria-label="Page 1">1</a>
      </li>
      <li className="pagination__item">
        <a href="#" className="pagination__link is-active" aria-label="Page 2" aria-current="page">2</a>
      </li>
      <li className="pagination__item">
        <a href="#" className="pagination__link" aria-label="Page 3">3</a>
      </li>
      <li className="pagination__item pagination__next">
        <a href="#" className="pagination__link" aria-label="Next page">
          <span aria-hidden="true">→</span>
        </a>
      </li>
    </ul>
  </nav>
</div>

```html
<nav class="pagination pagination--outlined" aria-label="Pagination">...</nav>
```

### Compact Pagination

Grouped buttons with no spacing between items.

<div className="component-preview component-preview--center">
  <nav className="pagination pagination--compact" aria-label="Pagination">
    <ul className="pagination__list">
      <li className="pagination__item pagination__prev">
        <a href="#" className="pagination__link" aria-label="Previous page">
          <span aria-hidden="true">←</span>
        </a>
      </li>
      <li className="pagination__item">
        <a href="#" className="pagination__link" aria-label="Page 1">1</a>
      </li>
      <li className="pagination__item">
        <a href="#" className="pagination__link" aria-label="Page 2">2</a>
      </li>
      <li className="pagination__item">
        <a href="#" className="pagination__link is-active" aria-label="Page 3" aria-current="page">3</a>
      </li>
      <li className="pagination__item">
        <a href="#" className="pagination__link" aria-label="Page 4">4</a>
      </li>
      <li className="pagination__item">
        <a href="#" className="pagination__link" aria-label="Page 5">5</a>
      </li>
      <li className="pagination__item pagination__next">
        <a href="#" className="pagination__link" aria-label="Next page">
          <span aria-hidden="true">→</span>
        </a>
      </li>
    </ul>
  </nav>
</div>

```html
<nav class="pagination pagination--compact" aria-label="Pagination">...</nav>
```

## Alignment

### Center Aligned

<div className="component-preview component-preview--center">
  <nav className="pagination pagination--center"  aria-label="Pagination">
    <ul className="pagination__list">
      <li className="pagination__item pagination__prev">
        <a href="#" className="pagination__link" aria-label="Previous page">
          <span aria-hidden="true">←</span>
        </a>
      </li>
      <li className="pagination__item">
        <a href="#" className="pagination__link" aria-label="Page 1">1</a>
      </li>
      <li className="pagination__item">
        <a href="#" className="pagination__link is-active" aria-label="Page 2" aria-current="page">2</a>
      </li>
       <li className="pagination__item">
        <a href="#" className="pagination__link" aria-label="Page 3">3</a>
      </li>
      <li className="pagination__item pagination__next">
        <a href="#" className="pagination__link" aria-label="Next page">
          <span aria-hidden="true">→</span>
        </a>
      </li>
    </ul>
  </nav>
</div>

```html
<nav class="pagination pagination--center">...</nav>
```

### Right Aligned

<div className="component-preview component-preview--center"  style={{justifyContent: 'flex-end'}}>
  <nav className="pagination pagination--right"  aria-label="Pagination">
    <ul className="pagination__list">
        <li className="pagination__item pagination__prev">
        <a href="#" className="pagination__link" aria-label="Previous page">
            <span aria-hidden="true">←</span>
        </a>
        </li>
        <li className="pagination__item">
        <a href="#" className="pagination__link" aria-label="Page 1">1</a>
        </li>
        <li className="pagination__item">
        <a href="#" className="pagination__link is-active" aria-label="Page 2" aria-current="page">2</a>
        </li>
        <li className="pagination__item">
        <a href="#" className="pagination__link" aria-label="Page 3">3</a>
        </li>
        <li className="pagination__item pagination__next">
        <a href="#" className="pagination__link" aria-label="Next page">
            <span aria-hidden="true">→</span>
        </a>
        </li>
    </ul>
  </nav>
</div>

```html
<nav class="pagination pagination--right">...</nav>
```

## Combined Modifiers

Mixing multiple modifiers for custom styling.

### Small + Rounded + Center

<div className="component-preview component-preview--center">
  <nav className="pagination pagination--sm pagination--rounded pagination--center"  aria-label="Pagination">
    <ul className="pagination__list">
      <li className="pagination__item pagination__prev">
        <a href="#" className="pagination__link" aria-label="Previous page">
          <span aria-hidden="true">←</span>
        </a>
      </li>
      <li className="pagination__item">
        <a href="#" className="pagination__link" aria-label="Page 1">1</a>
      </li>
      <li className="pagination__item">
        <a href="#" className="pagination__link is-active" aria-label="Page 2" aria-current="page">2</a>
      </li>
      <li className="pagination__item">
        <a href="#" className="pagination__link" aria-label="Page 3">3</a>
      </li>
      <li className="pagination__item pagination__next">
        <a href="#" className="pagination__link" aria-label="Next page">
          <span aria-hidden="true">→</span>
        </a>
      </li>
    </ul>
  </nav>
</div>

```html
<nav class="pagination pagination--sm pagination--rounded pagination--center">
  ...
</nav>
```

### Large + Simple + Right

<div className="component-preview component-preview--center" style={{justifyContent: 'flex-end'}}>
  <nav className="pagination pagination--lg pagination--simple pagination--right" aria-label="Pagination">
    <ul className="pagination__list">
      <li className="pagination__item pagination__prev">
        <a href="#" className="pagination__link" aria-label="Previous page">
          <span aria-hidden="true">←</span>
          <span>Previous</span>
        </a>
      </li>
      <li className="pagination__item">
        <a href="#" className="pagination__link" aria-label="Page 1">1</a>
      </li>
      <li className="pagination__item">
        <a href="#" className="pagination__link" aria-label="Page 2">2</a>
      </li>
      <li className="pagination__item">
        <a href="#" className="pagination__link is-active" aria-label="Page 3" aria-current="page">3</a>
      </li>
      <li className="pagination__item pagination__next">
        <a href="#" className="pagination__link" aria-label="Next page">
          <span>Next</span>
          <span aria-hidden="true">→</span>
        </a>
      </li>
    </ul>
  </nav>
</div>

```html
<nav class="pagination pagination--lg pagination--simple pagination--right">
  ...
</nav>
```

## Usage Notes

### Accessibility

- Always use `<nav aria-label="Pagination">` for proper semantics.
- Use `<ol>` (ordered list) or `<ul>` for the pagination items.
- Include `aria-label` on each link describing the page number (e.g., "Page 1").
- Mark the current page with `aria-current="page"`.
- Use `is-active` class for the current page style.
- Use `is-disabled` class for disabled prev/next buttons.
- Hide decorative icons from screen readers with `aria-hidden="true"`.

### Available Modifiers

**Sizes:**

- `pagination--sm`: Small size (compact spacing)
- `pagination--lg`: Large size (spacious layout)

**Styles:**

- `pagination--rounded`: Fully rounded buttons
- `pagination--simple`: No borders, minimal style
- `pagination--outlined`: Border only, transparent background
- `pagination--compact`: Grouped buttons with no gaps

**Alignment:**

- `pagination--center`: Center horizontally
- `pagination--right`: Right align

### Best Practices

- Use ellipsis (...) for large page counts to avoid overwhelming the UI.
- Always show first and last page numbers when using an ellipsis.
- Disable prev button on the first page, and next button on the last page.
- Make the current page non-clickable with the `is-active` class.
- Consider mobile responsiveness - use smaller sizes on mobile devices.
- Show 5-7 page numbers maximum for optimal UX.
- Provide clear visual feedback for hover and active states.
