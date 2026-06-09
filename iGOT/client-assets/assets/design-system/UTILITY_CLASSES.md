# Design System — Utility Classes & Tokens Reference

Use these CSS custom properties (variables) when developing components.
They automatically adapt between light and dark themes via `[data-theme="light"]` / `[data-theme="dark"]`.

---

## 1. Colors — Primary

| Variable | Light | Dark |
|----------|-------|------|
| `--color-primary-50` | #E8EDF6 | #E8EDF6 |
| `--color-primary-100` | #B8C8E2 | #B8C8E2 |
| `--color-primary-200` | #96ADD4 | #96ADD4 |
| `--color-primary-300` | #6687C0 | #6687C0 |
| `--color-primary-400` | #4970B4 | #4970B4 |
| `--color-primary-500` | #1B4CA1 | #1B4CA1 |
| `--color-primary-600` | #194593 | #194593 |
| `--color-primary-700` | #133672 | #133672 |
| `--color-primary-800` | #0F2A59 | #0F2A59 |
| `--color-primary-900` | #0B2044 | #0B2044 |

**Usage:**
```css
.my-element { color: var(--color-primary-500); }
```

---

## 2. Colors — Secondary (Orange)

| Variable | Light | Dark |
|----------|-------|------|
| `--color-secondary-50` | #FEF5EA | #FEF5EA |
| `--color-secondary-100` | #FBDEBF | #FBDEBF |
| `--color-secondary-300` | #F7B974 | #F7B974 |
| `--color-secondary-500` | #F3962F | #F3962F |
| `--color-secondary-700` | #AD6B21 | #AD6B21 |
| `--color-secondary-900` | #663F14 | #663F14 |

---

## 3. Colors — Tertiary (Dark Navy)

| Variable | Light | Dark |
|----------|-------|------|
| `--color-tertiary-50` | #E8E9EB | #E8E9EB |
| `--color-tertiary-300` | #666A76 | #666A76 |
| `--color-tertiary-500` | #1B2133 | #1B2133 |
| `--color-tertiary-700` | #131724 | #131724 |
| `--color-tertiary-900` | #0B0E15 | #0B0E15 |

---

## 4. Colors — System / Status

| Variable | Value | Usage |
|----------|-------|-------|
| `--color-error-red-500` | #D13924 | Error states |
| `--color-success-green-500` | #1D8923 | Success states |
| `--color-warning-yellow-500` | #E99E38 | Warnings |
| `--color-info-blue-500` | #0A5396 | Information |

**With opacity variants:** `-o-16`, `-o-24`, `-o-32`, `-o-40`, `-o-48`

```css
.error-bg { background: var(--color-error-red-o-16); }
.error-text { color: var(--color-error-red-500); }
```

---

## 5. Colors — Accents

| Variable | Value |
|----------|-------|
| `--color-accents-red` | #FF383C |
| `--color-accents-orange` | #FF8D28 |
| `--color-accents-yellow` | #FFCC00 |
| `--color-accents-green` | #34C759 |
| `--color-accents-mint` | #00C8B3 |
| `--color-accents-teal` | #00C3D0 |
| `--color-accents-cyan` | #00C0E8 |
| `--color-accents-blue` | #0088FF |
| `--color-accents-indigo` | #6155F5 |
| `--color-accents-purple` | #CB30E0 |
| `--color-accents-pink` | #FF2D55 |
| `--color-accents-brown` | #AC7F5E |

---

## 6. Background Colors (Theme-Aware)

| Variable | Light | Dark |
|----------|-------|------|
| `--surface-primary` | #FFFFFF | #1B2133 |
| `--surface-secondary` | #EFF3F9 | #252D3F |
| `--surface-tertiary` | #F5F5F5 | #333D4C |
| `--surface-inverse` | #1B2133 | #FFFFFF |
| `--environment-application-backgrounds-system-background-1` | #FFFFFF | #0B2044 |
| `--environment-application-backgrounds-card-background` | #FFFFFF | #133672 |
| `--environment-application-backgrounds-other-background` | #1B4CA1 | #133672 |

**Usage:**
```css
.page { background-color: var(--surface-primary); }
.card { background-color: var(--environment-application-backgrounds-card-background); }
.sidebar { background-color: var(--surface-secondary); }
```

---

## 7. Text Colors (Theme-Aware)

| Variable | Light | Dark | Usage |
|----------|-------|------|-------|
| `--text-bandw-black-display` | rgba(0,0,0,0.96) | rgba(255,255,255,0.96) | Large display text |
| `--text-bandw-black-heading` | rgba(0,0,0,0.96) | rgba(255,255,255,0.96) | Headings |
| `--text-bandw-black-title` | rgba(0,0,0,0.88) | rgba(255,255,255,0.88) | Titles |
| `--text-bandw-black-sub-heading` | rgba(0,0,0,0.80) | rgba(255,255,255,0.80) | Subheadings |
| `--text-bandw-black-body` | rgba(0,0,0,0.80) | rgba(255,255,255,0.80) | Body text |
| `--text-bandw-black-captions` | rgba(0,0,0,0.72) | rgba(255,255,255,0.72) | Captions |
| `--text-bandw-black-lables` | rgba(0,0,0,0.72) | rgba(255,255,255,0.72) | Labels |
| `--text-bandw-black-fine-print` | rgba(0,0,0,0.72) | rgba(255,255,255,0.72) | Fine print |
| `--text-system-text-disabled` | rgba(0,0,0,0.48) | rgba(255,255,255,0.48) | Disabled text |
| `--text-system-text-success` | #1D8923 | #1D8923 | Success text |
| `--text-system-text-error` | #D13924 | #D13924 | Error text |
| `--text-system-text-warning` | #E99E38 | #E99E38 | Warning text |

**Permanent (don't flip with theme):**
- `--text-permanent-black-*` — Always dark text
- `--text-permanent-white-*` — Always light text

**Usage:**
```css
h1 { color: var(--text-bandw-black-heading); }
p { color: var(--text-bandw-black-body); }
.caption { color: var(--text-bandw-black-captions); }
```

---

## 8. Button Colors (Theme-Aware)

| Variable | Light | Dark |
|----------|-------|------|
| `--environment-button-primary-filled-primary` | #1B4CA1 | #FFFFFF |
| `--environment-button-primary-filled-primary-hover` | #133672 | #FFFFFF |
| `--environment-button-primary-filled-primary-disabled` | rgba(27,76,161,0.48) | rgba(255,255,255,0.48) |
| `--environment-button-secondary-filled-secondary` | #F3962F | #F3962F |
| `--environment-button-secondary-filled-secondary-hover` | #AD6B21 | #AD6B21 |
| `--text-button-text-primary-white` | #FFFFFF | #1B4CA1 |
| `--text-button-text-link` | #1B4CA1 | #FFFFFF |

---

## 9. Border & Divider (Theme-Aware)

| Variable | Light | Dark |
|----------|-------|------|
| `--border-default` | rgba(0,0,0,0.08) | rgba(255,255,255,0.08) |
| `--border-strong` | rgba(0,0,0,0.16) | rgba(255,255,255,0.16) |
| `--border-focus` | #1B4CA1 | #6687C0 |
| `--environment-border-and-divider-default-1` | rgba(0,0,0,0.16) | rgba(255,255,255,0.24) |
| `--environment-border-and-divider-focused` | #0B2044 | #B8C8E2 |
| `--environment-border-and-divider-disable` | rgba(0,0,0,0.24) | rgba(255,255,255,0.08) |

**Usage:**
```css
.card { border: var(--stroke-1) solid var(--border-default); }
.input:focus { border-color: var(--border-focus); }
```

---

## 10. Icon Colors (Theme-Aware)

| Variable | Light | Dark |
|----------|-------|------|
| `--environment-icon-overall-primary-bandw` | #000000 | #FFFFFF |
| `--environment-icon-overall-secondary-bandw` | rgba(0,0,0,0.72) | rgba(255,255,255,0.72) |
| `--environment-icon-permanent-permanent-blue-icon` | #1B4CA1 | #1B4CA1 |
| `--environment-icon-system-success` | #1D8923 | #1D8923 |
| `--environment-icon-system-error` | #D13924 | #D13924 |

---

## 11. Typography — Font Sizes

| Variable | Desktop (1440+) | Tablet (426-1023) | Mobile (≤425) |
|----------|----------------|-------------------|---------------|
| `--font-size-display-1` | 48px | 36px | 30px |
| `--font-size-dispaly-2` | 40px | 30px | 28px |
| `--font-size-heading-1` | 32px | 28px | 24px |
| `--font-size-heading-2` | 28px | 24px | 20px |
| `--font-size-title-1` | 24px | 20px | 18px |
| `--font-size-title-2` | 20px | 16px | 16px |
| `--font-size-sub-heading-1` | 18px | 16px | 16px |
| `--font-size-sub-heading-2` | 16px | 14px | 14px |
| `--font-size-body-1` | 16px | 16px | 16px |
| `--font-size-body-2` | 14px | 14px | 14px |
| `--font-size-button-1` | 16px | 16px | 16px |
| `--font-size-button-2` | 14px | 14px | 14px |
| `--font-size-caption-1` | 12px | 12px | 12px |
| `--font-size-label-1` | 12px | 12px | 12px |
| `--font-size-fine-print-1` | 12px | 12px | 12px |

**Usage:**
```css
h1 { font-size: var(--font-size-heading-1); }
h2 { font-size: var(--font-size-heading-2); }
.title { font-size: var(--font-size-title-1); }
p { font-size: var(--font-size-body-1); }
.small { font-size: var(--font-size-caption-1); }
```

---

## 12. Font Families

| Variable | Value |
|----------|-------|
| `--font-family-primary` | 'Lato', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif |
| `--font-family-heading` | 'Montserrat', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif |
| `--font-family-mono` | 'Fira Code', Menlo, Monaco, Consolas, monospace |

**Usage:**
```css
body { font-family: var(--font-family-primary); }
h1, h2, h3 { font-family: var(--font-family-heading); }
code { font-family: var(--font-family-mono); }
```

---

## 13. Spacing Scale

| Variable | Value | Usage |
|----------|-------|-------|
| `--space-0` | 0px | None |
| `--space-2` | 2px | Hairline |
| `--space-4` | 4px | Tight |
| `--space-8` | 8px | Small |
| `--space-12` | 12px | Medium-small |
| `--space-16` | 16px | Medium |
| `--space-20` | 20px | Medium-large |
| `--space-24` | 24px | Large |
| `--space-32` | 32px | X-Large |
| `--space-40` | 40px | XX-Large |
| `--space-48` | 48px | XXX-Large |
| `--space-64` | 64px | Huge |
| `--space-128` | 128px | Maximum |

**Usage:**
```css
.section { margin-bottom: var(--space-24); }
.card { padding: var(--space-16); }
.items > * + * { margin-top: var(--space-8); }
```

---

## 14. Padding Tokens

| Variable | Value |
|----------|-------|
| `--padding-no-padding` | 0px |
| `--padding-xs-padding` | 4px |
| `--padding-s-padding` | 8px |
| `--padding-m-padding` | 12px |
| `--padding-l-padding` | 16px |
| `--padding-xl-padding` | 20px |
| `--padding-xxl-padding` | 24px |
| `--padding-xxxl-padding` | 32px |

**Usage:**
```css
.card { padding: var(--padding-l-padding); }
.chip { padding: var(--padding-xs-padding) var(--padding-s-padding); }
```

---

## 15. Gap Tokens

| Variable | Value |
|----------|-------|
| `--gap-no-gap` | 0px |
| `--gap-xs-gap` | 4px |
| `--gap-s-gap` | 8px |
| `--gap-m-gap` | 12px |
| `--gap-l-gap` | 16px |
| `--gap-xl-gap` | 20px |
| `--gap-xxl-gap` | 24px |
| `--gap-xxxl-gap` | 32px |

**Usage:**
```css
.flex-row { display: flex; gap: var(--gap-m-gap); }
.grid { display: grid; gap: var(--gap-l-gap); }
```

---

## 16. Border Radius

| Variable | Value | Usage |
|----------|-------|-------|
| `--radius-4` | 4px | Subtle rounding |
| `--radius-8` | 8px | Cards, inputs |
| `--radius-12` | 12px | Containers |
| `--radius-16` | 16px | Large cards |
| `--radius-999` | 999px | Pills, circles |

**Usage:**
```css
.card { border-radius: var(--radius-8); }
.chip { border-radius: var(--radius-999); }
.avatar { border-radius: var(--radius-999); }
```

---

## 17. Stroke / Border Width

| Variable | Value |
|----------|-------|
| `--stroke-1` | 1px |
| `--stroke-2` | 2px |

---

## 18. Icon Sizes

| Variable | Value | Usage |
|----------|-------|-------|
| `--icon-sm` | 16px | Inline small icons |
| `--icon-md` | 20px | Default icons |
| `--icon-lg` | 24px | Standard mat-icon |
| `--icon-xl` | 32px | Featured icons |
| `--icon-xxl` | 40px | Hero icons |

**Usage:**
```css
.icon-small { width: var(--icon-sm); height: var(--icon-sm); }
mat-icon { font-size: var(--icon-lg); }
```

---

## 19. Grid System (Responsive)

| Variable | Mobile (≤425) | Tablet (426-1023) | Desktop (1024+) |
|----------|---------------|-------------------|-----------------|
| `--grid-grid-column` | 4 | 6 | 12 |
| `--grid-grid-gutter` | 20px | 16px | 16px |
| `--grid-grid-margin-landr` | 20px | 16px | 16px |

**Usage:**
```css
.container {
  display: grid;
  grid-template-columns: repeat(var(--grid-grid-column), 1fr);
  gap: var(--grid-grid-gutter);
  padding-left: var(--grid-grid-margin-landr);
  padding-right: var(--grid-grid-margin-landr);
}
```

---

## 20. Fills (Theme-Aware) — Environment Colors

These flip between light and dark automatically:

```css
/* Primary fills — flip shades between themes */
background: var(--environment-all-fills-primary-primary-50-900);  /* Light: #E8EDF6, Dark: #0B2044 */
background: var(--environment-all-fills-primary-primary-500-400); /* Light: #1B4CA1, Dark: #4970B4 */

/* Cards */
background: var(--environment-cards-overall-cards-primary);       /* Light: #E8EDF6, Dark: #0F121C */

/* Overlay */
background: var(--environment-all-fills-overlay-backdrop);        /* rgba(0,0,0,0.32) */
```

---

## 21. Black & White with Opacity

| Pattern | Example |
|---------|---------|
| `--color-black-opacity-{8-96}` | `var(--color-black-opacity-16)` → rgba(0,0,0,0.16) |
| `--color-white-white-o-{8-96}` | `var(--color-white-white-o-16)` → rgba(255,255,255,0.16) |
| `--color-primary-o-{8-96}` | `var(--color-primary-o-16)` → rgba(27,76,161,0.16) |

---

## Quick Start Example

```scss
.my-card {
  background-color: var(--environment-application-backgrounds-card-background);
  border: var(--stroke-1) solid var(--border-default);
  border-radius: var(--radius-8);
  padding: var(--padding-l-padding);
  
  h3 {
    font-family: var(--font-family-heading);
    font-size: var(--font-size-title-2);
    color: var(--text-bandw-black-heading);
    margin-bottom: var(--space-8);
  }
  
  p {
    font-family: var(--font-family-primary);
    font-size: var(--font-size-body-1);
    color: var(--text-bandw-black-body);
  }
  
  .icon {
    color: var(--environment-icon-overall-primary-bandw);
    font-size: var(--icon-lg);
  }
  
  .btn-primary {
    background-color: var(--environment-button-primary-filled-primary);
    color: var(--text-button-text-primary-white);
    border-radius: var(--radius-4);
    padding: var(--padding-s-padding) var(--padding-l-padding);
    
    &:hover {
      background-color: var(--environment-button-primary-filled-primary-hover);
    }
    
    &:disabled {
      background-color: var(--environment-button-primary-filled-primary-disabled);
    }
  }
}
```

---

## Font Size Accessibility (Header Controls)

The header provides A-/A+ buttons that apply these body classes:
- `x-small-typography` — base 10px
- `small-typography` — base 12px  
- `normal-typography` — base 14px (default)
- `large-typography` — base 16px
- `x-large-typography` — base 18px

These are managed by `BtnSettingsService` and stored in `localStorage('setting')`.
