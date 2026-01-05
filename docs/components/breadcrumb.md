---
sidebar_label: "Breadcrumb"
---

# Breadcrumb

Breadcrumbs indicate the current page's location within a navigational hierarchy.

## Basic Usage

<div className="component-preview component-preview--center">
  <nav className="breadcrumb" aria-label="Breadcrumb">
    <ol className="breadcrumb__list">
      <li className="breadcrumb__item">
        <a href="#" className="breadcrumb__link">Home</a>
        <span className="breadcrumb__separator" aria-hidden="true"></span>
      </li>
      <li className="breadcrumb__item">
        <a href="#" className="breadcrumb__link">Library</a>
         <span className="breadcrumb__separator" aria-hidden="true"></span>
      </li>
      <li className="breadcrumb__item">
         <a href="#" className="breadcrumb__link is-active" aria-current="page">Data</a>
         <span className="breadcrumb__separator" aria-hidden="true"></span>
      </li>
    </ol>
  </nav>
</div>

```html
<nav class="breadcrumb" aria-label="Breadcrumb">
  <ol class="breadcrumb__list">
    <li class="breadcrumb__item">
      <a href="#" class="breadcrumb__link">Home</a>
      <span class="breadcrumb__separator" aria-hidden="true"></span>
    </li>
    <li class="breadcrumb__item">
      <a href="#" class="breadcrumb__link">Library</a>
      <span class="breadcrumb__separator" aria-hidden="true"></span>
    </li>
    <li class="breadcrumb__item">
      <a href="#" class="breadcrumb__link is-active" aria-current="page"
        >Data</a
      >
      <span class="breadcrumb__separator" aria-hidden="true"></span>
    </li>
  </ol>
</nav>
```

## Separator Styles

You can change the separator style using modifiers on the `.breadcrumb` container.

### Slash (Default)

The default separator is a slash `/`. You can also explicitly use `.breadcrumb--slash`.

### Chevron

<div className="component-preview component-preview--center">
  <nav className="breadcrumb breadcrumb--chevron" aria-label="Breadcrumb">
    <ol className="breadcrumb__list">
      <li className="breadcrumb__item">
        <a href="#" className="breadcrumb__link">Home</a>
        <span className="breadcrumb__separator"></span>
      </li>
      <li className="breadcrumb__item">
        <a href="#" className="breadcrumb__link">Category</a>
         <span className="breadcrumb__separator"></span>
      </li>
      <li className="breadcrumb__item">
         <span className="breadcrumb__link is-active">Page</span>
      </li>
    </ol>
  </nav>
</div>

```html
<nav class="breadcrumb breadcrumb--chevron">...</nav>
```

### Arrow

<div className="component-preview component-preview--center">
  <nav className="breadcrumb breadcrumb--arrow" aria-label="Breadcrumb">
    <ol className="breadcrumb__list">
      <li className="breadcrumb__item">
        <a href="#" className="breadcrumb__link">Home</a>
        <span className="breadcrumb__separator"></span>
      </li>
      <li className="breadcrumb__item">
        <span className="breadcrumb__link is-active">Active</span>
      </li>
    </ol>
  </nav>
</div>

```html
<nav class="breadcrumb breadcrumb--arrow">...</nav>
```

### Dash

<div className="component-preview component-preview--center">
  <nav className="breadcrumb breadcrumb--dash" aria-label="Breadcrumb">
    <ol className="breadcrumb__list">
      <li className="breadcrumb__item">
        <a href="#" className="breadcrumb__link">Home</a>
        <span className="breadcrumb__separator"></span>
      </li>
      <li className="breadcrumb__item">
        <span className="breadcrumb__link is-active">Active</span>
      </li>
    </ol>
  </nav>
</div>

```html
<nav class="breadcrumb breadcrumb--dash">...</nav>
```

## Sizes

### Small

<div className="component-preview component-preview--center">
  <nav className="breadcrumb breadcrumb--sm" aria-label="Breadcrumb">
    <ol className="breadcrumb__list">
      <li className="breadcrumb__item">
        <a href="#" className="breadcrumb__link">Home</a>
        <span className="breadcrumb__separator"></span>
      </li>
      <li className="breadcrumb__item">
        <span className="breadcrumb__link is-active">Page</span>
      </li>
    </ol>
  </nav>
</div>

```html
<nav class="breadcrumb breadcrumb--sm">...</nav>
```

### Large

<div className="component-preview component-preview--center">
  <nav className="breadcrumb breadcrumb--lg" aria-label="Breadcrumb">
    <ol className="breadcrumb__list">
      <li className="breadcrumb__item">
        <a href="#" className="breadcrumb__link">Home</a>
        <span className="breadcrumb__separator"></span>
      </li>
      <li className="breadcrumb__item">
        <span className="breadcrumb__link is-active">Page</span>
      </li>
    </ol>
  </nav>
</div>

```html
<nav class="breadcrumb breadcrumb--lg">...</nav>
```
