# Mage ui

> ⚠️ Historical: created when I was 12–13 (nostalgic/learning project).
> Not actively maintained — use at your own risk (might be good idea).


Short description...

# Modern UI CSS Library Documentation

## Table of Contents
1. [Design Tokens](#design-tokens)
2. [Layout](#layout)
3. [Components](#components)
4. [Typography](#typography)
4. [Utilities](#utilities)
5. [Dark Mode](#dark-mode)

## Design Tokens

### Colors
The library provides a comprehensive color system with primary, secondary, and semantic colors:

```css
--primary: #0066FF
--primary-light: #4D94FF
--primary-dark: #0047B3
--secondary: #6C757D
```

**Semantic Colors:**
- `--success`: #28A745
- `--danger`: #DC3545
- `--warning`: #FFC107
- `--info`: #17A2B8

**Grays:**
- `--gray-100` to `--gray-900`: A scale from light (#F8F9FA) to dark (#212529)

### Typography
**Font Families:**
```css
--font-family-base: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif
```

**Font Sizes:**
- Base: `--font-size-base: 1rem`
- Large: `--font-size-lg: 1.25rem`
- Small: `--font-size-sm: 0.875rem`

**Font Weights:**
- Normal: `--font-weight-normal: 400`
- Medium: `--font-weight-medium: 500`
- Bold: `--font-weight-bold: 700`

### Spacing
Consistent spacing scale:
- `--spacing-1`: 0.25rem
- `--spacing-2`: 0.5rem
- `--spacing-3`: 1rem
- `--spacing-4`: 1.5rem
- `--spacing-5`: 3rem

### Borders & Shadows
**Border Radius:**
- Default: `--border-radius: 0.5rem`
- Large: `--border-radius-lg: 0.75rem`
- Small: `--border-radius-sm: 0.25rem`

**Shadows:**
- Small: `--shadow-sm: 0 1px 2px rgba(0, 0, 0, 0.05)`
- Default: `--shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1)`
- Large: `--shadow-lg: 0 10px 15px -3px rgba(0, 0, 0, 0.1)`

## Layout

### Grid System
The library includes a flexible grid system based on CSS Flexbox:

```html
<div class="container">
  <div class="row">
    <div class="col">Column 1</div>
    <div class="col">Column 2</div>
  </div>
</div>
```

**Breakpoints:**
- Small (sm): 576px
- Medium (md): 768px
- Large (lg): 992px
- Extra Large (xl): 1200px

## Components

### Buttons
Basic button structure with variants:

```html
<button class="btn btn-primary">Primary Button</button>
```

**Available Classes:**
- `.btn`: Base button styles
- `.btn-primary`: Primary colored button

### Cards
Card components for contained content:

```html
<div class="card">
  <div class="card-body">
    <h5 class="card-title">Card Title</h5>
    <p class="card-text">Card content goes here.</p>
  </div>
</div>
```

### Forms
Form controls with consistent styling:

```html
<input class="form-control" type="text" placeholder="Enter text">
```

### Navigation
Navigation components including basic nav and navbar:

```html
<nav class="navbar">
  <ul class="nav">
    <li><a class="nav-link" href="#">Link 1</a></li>
    <li><a class="nav-link" href="#">Link 2</a></li>
  </ul>
</nav>
```

### Modals
Modal dialog component:

```html
<div class="modal">
  <div class="modal-content">
    <!-- Modal content here -->
  </div>
</div>
```

To show modal: Add `.show` class to `.modal`

## Typography

Heading sizes:
- `h1, .h1`: 2.5rem
- `h2, .h2`: 2rem
- `h3, .h3`: 1.75rem
- `h4, .h4`: 1.5rem
- `h5, .h5`: 1.25rem
- `h6, .h6`: 1rem

## Utilities

### Margin Utilities
- `.mt-{1-5}`: Margin top
- `.mb-{1-5}`: Margin bottom

### Padding Utilities
- `.p-{1-5}`: Padding on all sides

### Display Utilities
- `.d-flex`: Display flex
- `.d-none`: Display none
- `.d-block`: Display block

### Flex Utilities
- `.align-items-center`: Align items center
- `.justify-content-center`: Justify content center
- `.justify-content-between`: Justify content space-between

### Text Utilities
- `.text-center`: Center text alignment
- `.text-left`: Left text alignment
- `.text-right`: Right text alignment

### Animation
```css
.fade-in {
  animation: fadeIn 0.3s ease-in-out;
}
```

## Dark Mode

The library includes automatic dark mode support using `prefers-color-scheme`. Dark mode adjusts colors automatically:

```css
@media (prefers-color-scheme: dark) {
  :root {
    --primary: #4D94FF;
    --white: #1A1A1A;
    --gray-900: #F8F9FA;
    /* ... other color adjustments */
  }
}
```

## Best Practices

1. Use the provided CSS variables for consistency
2. Leverage the utility classes for quick styling
3. Follow the responsive breakpoints for proper mobile support
4. Use semantic components (buttons, cards, forms) for better accessibility
5. Test both light and dark mode when implementing new features
