
# CSS Naming Convention Standard

This standard defines how CSS classes are named across Angry Monkey projects to keep HTML and LESS code clean, scalable, and easy to maintain.

## Objectives

- Keep markup readable and predictable.
- Reduce selector conflicts and side effects.
- Keep styles modular and easy to extend.
- Support efficient collaboration across teams.

## Core Naming Rules

### 1. Use a clear block class as the parent

Use one root class name per component with no separator in the block name.

```html
<div class="product-card"></div>
```

### 2. Name child elements with a single dash

Child elements are derived from the parent class using -.

```html
<div class="product-card">
  <p class="product-card-description">Fast, lightweight, durable.</p>
  <ul class="product-card-items">
    <li class="product-card-item">Item 1</li>
  </ul>
</div>
```

### 3. Use modifiers as standalone underscore-prefixed classes

Modifiers represent state or variation and must be added as separate classes.

```html
<button class="button button-primary _active">Save</button>
<p class="product-card-description _color-black">Description</p>
```

## LESS Authoring Pattern

Use nested LESS to keep relationships clear.

```less
.product-card {
  &-description {
    &._color {
      &-black {}
    }
  }

  &-items {}

  &-item {
    &._active {}
    &._primary {}
  }
}
```

## Content-Sectioning Rule

For semantic sectioning elements inside known structures (for example h1, header, footer), avoid unnecessary class names unless they need a reusable style identity.

```html
<div class="article">
  <h1>Title</h1>
  <p class="article-description">Summary</p>
</div>
```

## Avoid These Patterns

### 1. Do not use orphan modifiers

```css
/* Correct */
.button._disabled {}

/* Incorrect */
._disabled {}
```

### 2. Avoid deep chained element names

```html
<!-- Correct -->
<li class="menu-item">Home</li>

<!-- Avoid -->
<li class="menu-items-item">Home</li>
```

### 3. Prefer scoped page styles under main when page-specific

```less
main {
  .checkout-form {}
  .checkout-summary {}
}
```

## File and Implementation Guidance

- Author styles in .less files, never directly in .css source files.
- Keep class names lowercase and hyphenated.
- Keep naming expressive but concise.
- Use consistent naming throughout a component tree.

## Governance

- This is the canonical CSS naming standard for Angry Monkey Cloud managed documentation.
- New UI patterns should align with this format unless a documented exception is approved.
