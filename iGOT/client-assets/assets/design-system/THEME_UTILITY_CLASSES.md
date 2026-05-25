# Theme-Aware Utility Classes Reference

All classes below **automatically adapt** between light and dark modes. No need to write separate styles for each theme.

---

## How It Works

These classes use CSS custom properties internally. When `data-theme="dark"` is set on `<html>`, the variables resolve to dark-mode values automatically.

```html
<!-- This paragraph is blue in light mode, lighter blue in dark mode -->
<p class="text-primary">Hello World</p>

<!-- This card has correct bg in both themes -->
<div class="bg-card bordered">Content</div>
```

---

## Text Colors

### Semantic Text (auto-flips with theme)

| Class | Light Mode | Dark Mode | Usage |
|-------|-----------|-----------|-------|
| `.text-display` | rgba(0,0,0,0.96) | rgba(255,255,255,0.96) | Large display text |
| `.text-heading` | rgba(0,0,0,0.96) | rgba(255,255,255,0.96) | Headings (h1-h3) |
| `.text-title` | rgba(0,0,0,0.88) | rgba(255,255,255,0.88) | Titles |
| `.text-sub-heading` | rgba(0,0,0,0.80) | rgba(255,255,255,0.80) | Subheadings |
| `.text-body` | rgba(0,0,0,0.80) | rgba(255,255,255,0.80) | Body paragraphs |
| `.text-caption` | rgba(0,0,0,0.72) | rgba(255,255,255,0.72) | Captions |
| `.text-label` | rgba(0,0,0,0.72) | rgba(255,255,255,0.72) | Form labels |
| `.text-fine-print` | rgba(0,0,0,0.72) | rgba(255,255,255,0.72) | Fine print |
| `.text-disabled` | rgba(0,0,0,0.48) | rgba(255,255,255,0.48) | Disabled text |

```html
<h1 class="text-heading">Page Title</h1>
<p class="text-body">This is body text that adapts to the theme.</p>
<span class="text-caption">Last updated: today</span>
<span class="text-disabled">Cannot edit</span>
```

### Status Text

| Class | Color | Usage |
|-------|-------|-------|
| `.text-success` | #1D8923 | Success messages |
| `.text-error` | #D13924 | Error messages |
| `.text-warning` | #E99E38 | Warning messages |
| `.text-info` | #0A5396 | Info messages |

```html
<span class="text-success">Saved successfully!</span>
<span class="text-error">Something went wrong</span>
```

### Primary / Secondary / Tertiary Text (theme-aware shades)

| Class | Light Mode | Dark Mode | Usage |
|-------|-----------|-----------|-------|
| `.text-primary` | #1B4CA1 (blue-500) | #4970B4 (blue-400) | Primary brand color |
| `.text-primary-light` | #6687C0 (blue-300) | #194593 (blue-600) | Lighter primary |
| `.text-primary-dark` | #133672 (blue-700) | #96ADD4 (blue-200) | Darker primary |
| `.text-secondary` | #F3962F (orange-500) | #F5AB59 (orange-400) | Secondary brand |
| `.text-secondary-light` | #F7B974 (orange-300) | #DD892B (orange-600) | Lighter secondary |
| `.text-secondary-dark` | #AD6B21 (orange-700) | #F9CF9F (orange-200) | Darker secondary |
| `.text-tertiary` | #1B2133 (navy-500) | #494D5C (navy-400) | Tertiary dark navy |

```html
<a class="text-primary" href="/learn">Start Learning</a>
<p class="text-secondary">Featured content</p>
<small class="text-primary-light">Subtitle text</small>
```

### Link Text

| Class | Light Mode | Dark Mode | Usage |
|-------|-----------|-----------|-------|
| `.text-link` | #1B4CA1 (blue) | #FFFFFF (white) | Hyperlinks |
| `.text-link-disabled` | rgba(27,76,161,0.48) | rgba(255,255,255,0.48) | Disabled links |

```html
<a class="text-link" href="/details">View Details</a>
```

### Permanent Text (does NOT change with theme)

| Class | Color | Usage |
|-------|-------|-------|
| `.text-permanent-black` | rgba(0,0,0,0.80) | Always dark text (e.g., on colored bg) |
| `.text-permanent-white` | rgba(255,255,255,0.80) | Always light text (e.g., on dark bg) |
| `.text-permanent-black-heading` | rgba(0,0,0,0.96) | Always dark heading |
| `.text-permanent-white-heading` | rgba(255,255,255,0.96) | Always light heading |
| `.text-white` | #FFFFFF | Pure white |
| `.text-black` | #000000 | Pure black |

```html
<div class="bg-primary-500">
  <h2 class="text-permanent-white-heading">On Blue Background</h2>
  <p class="text-permanent-white">This stays white regardless of theme</p>
</div>
```

### Accent Text Colors

| Class | Color |
|-------|-------|
| `.text-accent-red` | #FF383C |
| `.text-accent-orange` | #FF8D28 |
| `.text-accent-yellow` | #FFCC00 |
| `.text-accent-green` | #34C759 |
| `.text-accent-mint` | #00C8B3 |
| `.text-accent-teal` | #00C3D0 |
| `.text-accent-cyan` | #00C0E8 |
| `.text-accent-blue` | #0088FF |
| `.text-accent-indigo` | #6155F5 |
| `.text-accent-purple` | #CB30E0 |
| `.text-accent-pink` | #FF2D55 |

---

## Background Colors

### Surfaces (auto-flips with theme)

| Class | Light Mode | Dark Mode | Usage |
|-------|-----------|-----------|-------|
| `.bg-surface-primary` | #FFFFFF | #1B2133 | Page background |
| `.bg-surface-secondary` | #EFF3F9 | #252D3F | Sidebar, secondary areas |
| `.bg-surface-tertiary` | #F5F5F5 | #333D4C | Subtle highlights |
| `.bg-surface-inverse` | #1B2133 | #FFFFFF | Inverse containers |

```html
<main class="bg-surface-primary">
  <aside class="bg-surface-secondary">Sidebar</aside>
  <div class="bg-surface-tertiary">Highlighted section</div>
</main>
```

### Application Backgrounds

| Class | Light Mode | Dark Mode | Usage |
|-------|-----------|-----------|-------|
| `.bg-system` | #FFFFFF | #0B2044 | System background |
| `.bg-card` | #FFFFFF | #133672 | Card backgrounds |
| `.bg-other` | #1B4CA1 | #133672 | Other/banner backgrounds |

```html
<div class="bg-card bordered">
  <h3 class="text-heading">Course Card</h3>
  <p class="text-body">Course description here</p>
</div>
```

### Primary Fills (shades flip between light ↔ dark)

| Class | Light Mode | Dark Mode |
|-------|-----------|-----------|
| `.bg-primary-50` | #E8EDF6 | #0B2044 |
| `.bg-primary-100` | #B8C8E2 | #0F2A59 |
| `.bg-primary-200` | #96ADD4 | #133672 |
| `.bg-primary-300` | #6687C0 | #194593 |
| `.bg-primary-400` | #4970B4 | #1B4CA1 |
| `.bg-primary-500` | #1B4CA1 | #4970B4 |
| `.bg-primary-600` | #194593 | #6687C0 |
| `.bg-primary-700` | #133672 | #96ADD4 |
| `.bg-primary-800` | #0F2A59 | #B8C8E2 |
| `.bg-primary-900` | #0B2044 | #E8EDF6 |

```html
<!-- Light subtle blue bg in light mode, deep navy in dark mode -->
<div class="bg-primary-50">Subtle emphasis</div>

<!-- Strong blue in light mode, medium blue in dark mode -->
<div class="bg-primary-500 text-permanent-white">CTA Banner</div>
```

### Secondary Fills (Orange shades — flip)

| Class | Light Mode | Dark Mode |
|-------|-----------|-----------|
| `.bg-secondary-50` | #FEF5EA | #663F14 |
| `.bg-secondary-300` | #F7B974 | #DD892B |
| `.bg-secondary-400` | #F3962F | #F5AB59 |
| `.bg-secondary-500` | #AD6B21 | #F5AB59 |
| `.bg-secondary-900` | #663F14 | #FEF5EA |

### Tertiary Fills (Navy shades — flip)

| Class | Light Mode | Dark Mode |
|-------|-----------|-----------|
| `.bg-tertiary-50` | #E8E9EB | #0B0E15 |
| `.bg-tertiary-400` | #1B2133 | #494D5C |
| `.bg-tertiary-500` | #494D5C | #1B2133 |
| `.bg-tertiary-900` | #0B0E15 | #E8E9EB |

### Gray Fills (theme-aware)

| Class | Light Mode | Dark Mode |
|-------|-----------|-----------|
| `.bg-gray-50` | #000000 | #E8E9EB |
| `.bg-gray-100` | #333333 | #B0B0B0 |
| `.bg-gray-200` | #545454 | #8A8A8A |
| `.bg-gray-300` | #8A8A8A | #545454 |
| `.bg-gray-400` | #B0B0B0 | #333333 |
| `.bg-gray-500` | #E8E9EB | #000000 |

### System Status Backgrounds

| Class | Color | Usage |
|-------|-------|-------|
| `.bg-success` | #1D8923 | Success state bg |
| `.bg-error` | #D13924 | Error state bg |
| `.bg-warning` | #E99E38 | Warning state bg |
| `.bg-info` | #0A5396 | Information state bg |

### Accent Backgrounds

| Class | Color |
|-------|-------|
| `.bg-accent-red` | #FF383C |
| `.bg-accent-orange` | #FF8D28 |
| `.bg-accent-yellow` | #FFCC00 |
| `.bg-accent-green` | #34C759 |
| `.bg-accent-mint` | #00C8B3 |
| `.bg-accent-teal` | #00C3D0 |
| `.bg-accent-cyan` | #00C0E8 |
| `.bg-accent-blue` | #0088FF |
| `.bg-accent-indigo` | #6155F5 |
| `.bg-accent-purple` | #CB30E0 |
| `.bg-accent-pink` | #FF2D55 |
| `.bg-accent-brown` | #AC7F5E |

### Cards & Overlay

| Class | Usage |
|-------|-------|
| `.bg-card-primary` | Card surface (theme-aware) |
| `.bg-card-success` | Success card |
| `.bg-card-error` | Error card |
| `.bg-card-warning` | Warning card |
| `.bg-card-info` | Info card |
| `.bg-overlay` | Modal backdrop (rgba 0,0,0,0.32) |
| `.bg-white` | Always white |

---

## Border Classes

### Border Color Only (add your own `border-style` and `border-width`)

| Class | Light Mode | Dark Mode | Usage |
|-------|-----------|-----------|-------|
| `.border-default` | rgba(0,0,0,0.08) | rgba(255,255,255,0.08) | Subtle border |
| `.border-strong` | rgba(0,0,0,0.16) | rgba(255,255,255,0.16) | Visible border |
| `.border-focus` | #1B4CA1 | #6687C0 | Focus ring |
| `.border-divider` | rgba(0,0,0,0.16) | rgba(255,255,255,0.24) | Divider lines |
| `.border-focused` | #0B2044 | #B8C8E2 | Focused input |
| `.border-disabled` | rgba(0,0,0,0.24) | rgba(255,255,255,0.08) | Disabled input |

### Ready-to-use Borders (includes width + style + color)

| Class | Description |
|-------|-------------|
| `.bordered` | 1px solid default border |
| `.bordered-strong` | 1px solid strong border |
| `.bordered-focus` | 2px solid focus border |
| `.bordered-primary` | 1px solid primary color |
| `.bordered-secondary` | 1px solid secondary (orange) |

### Status Border Colors

| Class | Color |
|-------|-------|
| `.border-accent-success` | #1D8923 |
| `.border-accent-error` | #D13924 |
| `.border-accent-warning` | #E99E38 |
| `.border-accent-info` | #0A5396 |

```html
<div class="bg-card bordered">Default bordered card</div>
<input class="bordered-strong" placeholder="Input field" />
<div class="bordered-primary bg-primary-50">Primary outline card</div>
```

---

## Icon Colors

| Class | Light Mode | Dark Mode | Usage |
|-------|-----------|-----------|-------|
| `.icon-primary` | #000000 | #FFFFFF | Main icons (flips) |
| `.icon-secondary` | rgba(0,0,0,0.72) | rgba(255,255,255,0.72) | Secondary icons |
| `.icon-inverse` | #FFFFFF | #000000 | Inverse icons |
| `.icon-blue` | #1B4CA1 | #1B4CA1 | Permanent blue |
| `.icon-blue-disabled` | rgba(27,76,161,0.48) | same | Disabled blue |
| `.icon-white` | #FFFFFF | #FFFFFF | Always white |
| `.icon-black` | #000000 | #000000 | Always black |
| `.icon-success` | #1D8923 | #1D8923 | Success icon |
| `.icon-error` | #D13924 | #D13924 | Error icon |
| `.icon-warning` | #E99E38 | #E99E38 | Warning icon |
| `.icon-info` | #0A5396 | #0A5396 | Info icon |

```html
<mat-icon class="icon-primary">home</mat-icon>
<mat-icon class="icon-success">check_circle</mat-icon>
<mat-icon class="icon-error">error</mat-icon>
```

---

## Button Classes

### Filled Primary Button

```html
<button class="btn-filled-primary">Submit</button>
```

| State | Light Mode BG | Dark Mode BG |
|-------|--------------|--------------|
| Default | #1B4CA1 | #FFFFFF |
| Hover | #133672 | #FFFFFF |
| Disabled | rgba(27,76,161,0.48) | rgba(255,255,255,0.48) |

### Outlined Primary Button

```html
<button class="btn-outlined-primary">Cancel</button>
```

### Filled Secondary Button

```html
<button class="btn-filled-secondary">Action</button>
```

| State | BG Color |
|-------|----------|
| Default | #F3962F |
| Hover | #AD6B21 |
| Disabled | rgba(243,150,47,0.48) |

### Outlined Secondary Button

```html
<button class="btn-outlined-secondary">Secondary</button>
```

### Link Button

```html
<button class="btn-link">Learn More</button>
```

## Complete Examples

The following are complete, theme-aware, responsive components built exclusively with the iGOT Karmayogi utility classes. They adapt seamlessly to both Light and Dark theme configurations.

### 1. Premium Course Card
```html
<div class="bg-card bordered" style="border-radius: var(--radius-12); overflow: hidden; max-width: 360px; box-shadow: var(--shadow);">
  <!-- Gradient header block using Primary brand tokens -->
  <div class="bg-other" style="padding: var(--padding-xl-padding) var(--padding-l-padding); position: relative; display: flex; flex-direction: column; justify-content: flex-end; min-height: 130px; background: linear-gradient(135deg, var(--color-primary-600), var(--color-primary-800));">
    <span class="bg-accent-orange text-permanent-white" style="position: absolute; top: 12px; right: 12px; padding: 3px 8px; border-radius: var(--radius-4); font-size: 10px; font-weight: 700; text-transform: uppercase;">Featured</span>
    <span class="material-icons text-permanent-white" style="font-size: var(--icon-xxl); opacity: 0.8; margin-bottom: 8px;">insights</span>
    <h4 class="text-permanent-white-heading" style="font-family: var(--font-family-heading); font-size: var(--font-size-sub-heading-1); font-weight: 700;">Data Analytics in Governance</h4>
  </div>

  <div style="padding: var(--padding-l-padding); display: flex; flex-direction: column; gap: var(--gap-s-gap);">
    <div style="display: flex; align-items: center; justify-content: space-between;">
      <span class="text-caption" style="font-weight: 600;">Ministry of Finance</span>
      <div style="display: flex; align-items: center; gap: 2px;">
        <span class="material-icons icon-warning" style="font-size: 14px;">star</span>
        <span class="text-body" style="font-size: 12px; font-weight: 700;">4.8</span>
      </div>
    </div>
    <p class="text-body text-body-2" style="line-height: 1.5;">Master data-driven policymaking and statistical indicators for modern government administration Operations.</p>
    
    <!-- Theme-Aware Progress Tracker -->
    <div style="margin-bottom: var(--space-8);">
      <div style="display: flex; justify-content: space-between; font-size: 11px; margin-bottom: 4px;" class="text-caption">
        <span>Progress</span>
        <span style="font-weight: 700;" class="text-primary">65% Completed</span>
      </div>
      <div class="bg-surface-secondary" style="height: 6px; border-radius: var(--radius-999); overflow: hidden; width: 100%;">
        <div class="bg-primary-500" style="width: 65%; height: 100%; border-radius: var(--radius-999);"></div>
      </div>
    </div>

    <!-- Actions and Credits -->
    <div style="display: flex; gap: var(--gap-s-gap); margin-top: var(--space-8); align-items: center; justify-content: space-between;">
      <span class="bg-primary-50 text-primary" style="padding: var(--padding-xs-padding) var(--padding-s-padding); border-radius: var(--radius-4); font-size: 11px; font-weight: 700;">12 Credits</span>
      <div style="display: flex; gap: 6px;">
        <button class="btn-outlined-primary" style="padding: 6px 12px; font-size: 12px;">Syllabus</button>
        <button class="btn-filled-primary" style="padding: 6px 12px; font-size: 12px;">Resume</button>
      </div>
    </div>
  </div>
</div>
```

### 2. Dashboard Overview Grid
```html
<div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(130px, 1fr)); gap: 12px;">
  <!-- Active Learning Widget -->
  <div class="bg-card bordered" style="border-radius: var(--radius-8); padding: var(--padding-l-padding); display: flex; flex-direction: column; gap: 8px;">
    <div style="display: flex; align-items: center; justify-content: space-between;">
      <span class="text-caption" style="font-weight: 600;">Active Learning</span>
      <span class="material-icons icon-blue">school</span>
    </div>
    <h3 class="text-heading text-title-1" style="font-weight: 800; line-height: 1;">4 Courses</h3>
    <span class="text-caption text-success" style="font-weight: 700; font-size: 11px; display: inline-flex; align-items: center; gap: 2px;">
      <span class="material-icons" style="font-size: 14px;">trending_up</span> +1 this week
    </span>
  </div>

  <!-- Time Spent Widget -->
  <div class="bg-card bordered" style="border-radius: var(--radius-8); padding: var(--padding-l-padding); display: flex; flex-direction: column; gap: 8px;">
    <div style="display: flex; align-items: center; justify-content: space-between;">
      <span class="text-caption" style="font-weight: 600;">Time Spent</span>
      <span class="material-icons icon-success">schedule</span>
    </div>
    <h3 class="text-heading text-title-1" style="font-weight: 800; line-height: 1;">18.5 Hrs</h3>
    <span class="text-caption" style="font-size: 11px;">Target: 20 Hrs</span>
  </div>

  <!-- Certificates Widget -->
  <div class="bg-card bordered" style="border-radius: var(--radius-8); padding: var(--padding-l-padding); display: flex; flex-direction: column; gap: 8px;">
    <div style="display: flex; align-items: center; justify-content: space-between;">
      <span class="text-caption" style="font-weight: 600;">Certificates</span>
      <span class="material-icons icon-warning">workspace_premium</span>
    </div>
    <h3 class="text-heading text-title-1" style="font-weight: 800; line-height: 1;">3 Earned</h3>
    <span class="text-caption text-primary" style="font-weight: 700; font-size: 11px;">1 Pending review</span>
  </div>
</div>
```

### 3. Adaptive Alert Banner Center
```html
<!-- Success Alert Banner with Thick Left Edge -->
<div class="bg-card-success bordered border-accent-success" style="padding: var(--padding-m-padding); border-radius: var(--radius-8); display: flex; gap: var(--gap-s-gap); border-left-width: 4px;">
  <span class="material-icons icon-success" style="font-size: 20px; flex-shrink: 0;">check_circle</span>
  <div>
    <h5 class="text-success" style="font-weight: 700; font-size: 13px; margin-bottom: 2px;">Action Successful</h5>
    <p class="text-body" style="font-size: 12px;">Your registration form has been submitted and approved successfully.</p>
  </div>
</div>

<!-- Error Alert -->
<div class="bg-card-error bordered border-accent-error" style="padding: var(--padding-m-padding); border-radius: var(--radius-8); display: flex; gap: var(--gap-s-gap); border-left-width: 4px;">
  <span class="material-icons icon-error" style="font-size: 20px; flex-shrink: 0;">cancel</span>
  <div>
    <h5 class="text-error" style="font-weight: 700; font-size: 13px; margin-bottom: 2px;">Submission Failed</h5>
    <p class="text-body" style="font-size: 12px;">Unable to process request. Please check mandatory fields.</p>
  </div>
</div>

<!-- Info Alert -->
<div class="bg-card-info bordered border-accent-info" style="padding: var(--padding-m-padding); border-radius: var(--radius-8); display: flex; gap: var(--gap-s-gap); border-left-width: 4px;">
  <span class="material-icons icon-info" style="font-size: 20px; flex-shrink: 0;">info</span>
  <div>
    <h5 class="text-info" style="font-weight: 700; font-size: 13px; margin-bottom: 2px;">Maintenance Scheduled</h5>
    <p class="text-body" style="font-size: 12px;">iGOT platform will be offline for upgrades tonight from 12 AM to 2 AM.</p>
  </div>
</div>
```

### 4. User Profile & Trainer Biography
```html
<div class="bg-card bordered" style="border-radius: var(--radius-12); padding: 24px; max-width: 360px; display: flex; flex-direction: column; align-items: center; text-align: center; gap: 16px; box-shadow: var(--shadow);">
  <!-- Avatar badge container -->
  <div style="position: relative;">
    <div class="bg-primary-100 bordered" style="width: 80px; height: 80px; border-radius: var(--radius-999); display: flex; align-items: center; justify-content: center; font-size: 32px; font-weight: 800; color: var(--color-primary-600);">
      SK
    </div>
    <div class="bg-accent-green" style="width: 16px; height: 16px; border-radius: var(--radius-999); border: 2px solid var(--card-bg); position: absolute; bottom: 2px; right: 2px;"></div>
  </div>

  <!-- Profile headers -->
  <div>
    <h4 class="text-heading text-title-2" style="font-weight: 700; margin-bottom: 2px;">Shri Sandeep Kumar</h4>
    <span class="text-caption" style="font-weight: 600;">Sr. Administrator, Capacity Building Commission</span>
  </div>

  <!-- Tag catalog cluster -->
  <div style="display: flex; gap: 6px; flex-wrap: wrap; justify-content: center;">
    <span class="bg-primary-50 text-primary" style="padding: 2px 8px; border-radius: var(--radius-999); font-size: 11px; font-weight: 700;">Governance</span>
    <span class="bg-secondary-50 text-secondary" style="padding: 2px 8px; border-radius: var(--radius-999); font-size: 11px; font-weight: 700;">Policy Making</span>
    <span class="bg-tertiary-50 text-tertiary" style="padding: 2px 8px; border-radius: var(--radius-999); font-size: 11px; font-weight: 700;">Public Ethics</span>
  </div>

  <p class="text-body text-body-2" style="line-height: 1.5; margin: 0;">
    20+ years of public service instruction. Spearheading curriculum design for civil service administrative systems reforms.
  </p>

  <div style="width: 100%; border-top: 1px solid var(--divider); padding-top: 16px; display: flex; gap: var(--gap-s-gap);">
    <button class="btn-outlined-primary" style="flex: 1; font-size: 13px; height: 36px;">Send Message</button>
    <button class="btn-filled-primary" style="flex: 1; font-size: 13px; height: 36px;">View Courses</button>
  </div>
</div>
```

### 5. Segment/Tab Navigation
```html
<div class="bg-card bordered" style="border-radius: var(--radius-8); overflow: hidden; width: 100%;">
  <!-- Horizontal Segment Ribbon -->
  <div style="display: flex; border-bottom: 1px solid var(--divider); background: var(--surface-secondary);">
    <!-- Active Tab Selection -->
    <button class="tab-btn active" style="flex: 1; background: none; border: none; border-bottom: 3px solid var(--color-primary-500); padding: 12px 8px; font-family: var(--font-family-heading); font-size: 13px; font-weight: 700; color: var(--color-primary-500); cursor: pointer;">
      Overview
    </button>
    
    <!-- Inactive Tab Selection -->
    <button class="tab-btn" style="flex: 1; background: none; border: none; border-bottom: 3px solid transparent; padding: 12px 8px; font-family: var(--font-family-heading); font-size: 13px; font-weight: 600; color: var(--text-sub); cursor: pointer;">
      Syllabus
    </button>
    
    <button class="tab-btn" style="flex: 1; background: none; border: none; border-bottom: 3px solid transparent; padding: 12px 8px; font-family: var(--font-family-heading); font-size: 13px; font-weight: 600; color: var(--text-sub); cursor: pointer;">
      Resources
    </button>
  </div>

  <div style="padding: 20px;">
    <p class="text-body text-body-2" style="line-height: 1.6; margin: 0;">
      Content pane coordinates standard elements seamlessly.
    </p>
  </div>
</div>
```

### 6. Advanced Form Control Panel
```html
<div class="bg-card bordered" style="border-radius: var(--radius-12); padding: 24px; max-width: 380px; display: flex; flex-direction: column; gap: 16px; box-shadow: var(--shadow);">
  <h4 class="text-heading text-title-2" style="font-weight: 700; border-bottom: 1px solid var(--divider); padding-bottom: 8px;">Registration Details</h4>
  
  <!-- Default Labeled Input -->
  <div style="display: flex; flex-direction: column; gap: 6px;">
    <label class="text-label" style="font-weight: 600; font-size: 12px;">Full Name *</label>
    <input class="bordered-strong text-body bg-card" placeholder="Enter your full name" style="border-radius: var(--radius-4); padding: var(--padding-s-padding); outline: none; font-size: 14px;" />
  </div>
  
  <!-- Error Validation Field -->
  <div style="display: flex; flex-direction: column; gap: 6px;">
    <label class="text-label" style="font-weight: 600; font-size: 12px;">Email Address *</label>
    <input class="text-body bg-card" placeholder="name@domain" value="invalid-email-format" style="border: 1px solid var(--color-error-red-500); border-radius: var(--radius-4); padding: var(--padding-s-padding); outline: none; font-size: 14px;" />
    <span class="text-error" style="font-size: 11px; font-weight: 700; display: flex; align-items: center; gap: 4px;">
      <span class="material-icons" style="font-size: 14px;">error</span> Please enter a valid institutional email
    </span>
  </div>

  <!-- Select Dropdown Menu -->
  <div style="display: flex; flex-direction: column; gap: 6px;">
    <label class="text-label" style="font-weight: 600; font-size: 12px;">Designated Department</label>
    <select class="bordered-strong text-body bg-card" style="border-radius: var(--radius-4); padding: var(--padding-s-padding); outline: none; font-size: 14px;">
      <option>Capacity Building Division</option>
      <option>Department of Personnel & Training</option>
    </select>
  </div>

  <!-- Custom styled checkbox -->
  <label style="display: flex; align-items: flex-start; gap: 8px; cursor: pointer;">
    <input type="checkbox" checked style="margin-top: 3px; accent-color: var(--color-primary-500);" />
    <span class="text-body" style="font-size: 12.5px;">I agree to the iGOT training guidelines.</span>
  </label>

  <button class="btn-filled-primary" style="width: 100%; height: 40px; font-size: 14px;">Complete Registration</button>
</div>
```

### 7. Course Syllabus Tracker
```html
<div class="bg-card bordered" style="border-radius: var(--radius-10); overflow: hidden; width: 100%;">
  <!-- Module banner -->
  <div style="padding: 16px 20px; border-bottom: 1px solid var(--divider); display: flex; align-items: center; justify-content: space-between; background: var(--surface-secondary);">
    <div>
      <h4 class="text-heading text-sub-heading-1" style="font-weight: 700;">Module 2: Policy Directives</h4>
      <span class="text-caption">4 Lessons • 2 Hrs Total</span>
    </div>
    <span class="bg-primary-50 text-primary" style="padding: 4px 10px; border-radius: var(--radius-999); font-size: 11px; font-weight: 700;">In Progress</span>
  </div>

  <!-- Module rows -->
  <div style="display: flex; flex-direction: column;">
    <!-- Row: Completed Lesson -->
    <div style="display: flex; align-items: center; gap: 12px; padding: 14px 20px; border-bottom: 1px solid var(--divider); background: var(--surface-primary);">
      <span class="material-icons icon-success" style="font-size: 22px;">check_circle</span>
      <div style="flex: 1;">
        <h5 class="text-heading text-body-2" style="font-weight: 700; text-decoration: line-through; opacity: 0.7;">2.1 Introduction to Policy Directives</h5>
        <span class="text-caption text-success" style="font-size: 11px; font-weight: 600;">Completed (Score: 92%)</span>
      </div>
      <span class="text-caption" style="font-size: 12px;">15 mins</span>
    </div>
    
    <!-- Row: Active Lesson -->
    <div style="display: flex; align-items: center; gap: 12px; padding: 14px 20px; border-bottom: 1px solid var(--divider); background: var(--tag-bg);">
      <span class="material-icons icon-blue" style="font-size: 22px;">play_circle_filled</span>
      <div style="flex: 1;">
        <h5 class="text-primary text-body-2" style="font-weight: 800;">2.2 Drafting Effective Frameworks</h5>
        <span class="text-caption text-primary" style="font-size: 11px; font-weight: 700;">Active lesson (5 mins remaining)</span>
      </div>
      <span class="text-caption text-primary" style="font-size: 12px; font-weight: 700;">35 mins</span>
    </div>
    
    <!-- Row: Locked Lesson -->
    <div style="display: flex; align-items: center; gap: 12px; padding: 14px 20px; opacity: 0.6; background: var(--surface-primary);">
      <span class="material-icons icon-secondary" style="font-size: 22px;">lock</span>
      <div style="flex: 1;">
        <h5 class="text-disabled text-body-2" style="font-weight: 600;">2.3 Compliance Analysis and Audits</h5>
        <span class="text-caption" style="font-size: 11px;">Requires 2.2 Completion</span>
      </div>
      <span class="text-caption" style="font-size: 12px;">40 mins</span>
    </div>
  </div>
</div>
```

### 8. Confirmation Modal Sandbox
```html
<div class="bg-card bordered" style="border-radius: var(--radius-12); max-width: 380px; width: 100%; box-shadow: var(--shadow); overflow: hidden; display: flex; flex-direction: column;">
  <!-- Modal Header with Warning Icon -->
  <div style="padding: 16px 20px; border-bottom: 1px solid var(--divider); display: flex; align-items: center; justify-content: space-between;">
    <h4 class="text-heading text-title-2" style="font-family: var(--font-family-heading); font-weight: 700; display: flex; align-items: center; gap: 8px;">
      <span class="material-icons icon-error" style="font-size: 22px;">warning</span> Delete Enrollment
    </h4>
    <span class="material-icons icon-secondary" style="cursor: pointer; font-size: 20px;">close</span>
  </div>
  
  <!-- Modal Body Message -->
  <div style="padding: 20px; display: flex; flex-direction: column; gap: 12px;">
    <p class="text-body text-body-2" style="line-height: 1.5; margin: 0;">
      Are you sure you want to cancel your enrollment in <strong>"Ethics in Public Policy"</strong>?
    </p>
    <div class="bg-card-warning bordered border-accent-warning" style="padding: 10px 12px; border-radius: var(--radius-4); display: flex; gap: 8px; border-left-width: 3px;">
      <span class="material-icons icon-warning" style="font-size: 18px; margin-top: 1px;">warning</span>
      <span class="text-body" style="font-size: 11.5px;">This action is permanent. All completed progress will be lost.</span>
    </div>
  </div>

  <!-- Action Bar footer -->
  <div style="padding: 14px 20px; border-top: 1px solid var(--divider); background: var(--surface-secondary); display: flex; justify-content: flex-end; gap: 10px;">
    <button class="btn-outlined-primary" style="padding: 6px 16px; font-size: 13px;">Keep Enrolled</button>
    <button class="btn-filled-primary" style="padding: 6px 16px; font-size: 13px; background: var(--color-error-red-500); border-color: var(--color-error-red-500); color: #fff;">Confirm Delete</button>
  </div>
</div>
```

### 9. Data Table Course Row
```html
<div class="bg-card bordered" style="border-radius: var(--radius-8); width: 100%; overflow-x: auto; box-shadow: var(--shadow);">
  <table style="width: 100%; border-collapse: collapse; min-width: 440px;">
    <tbody>
      <tr class="bg-surface-primary">
        <!-- Thumbnail icon -->
        <td style="padding: 14px 16px; width: 64px; vertical-align: middle;">
          <div class="bg-primary-50 bordered-primary" style="width: 48px; height: 48px; border-radius: var(--radius-4); display: flex; align-items: center; justify-content: center;">
            <span class="material-icons icon-blue">menu_book</span>
          </div>
        </td>
        
        <!-- Description Info -->
        <td style="padding: 14px 12px; vertical-align: middle;">
          <div style="display: flex; flex-direction: column; gap: 2px;">
            <h5 class="text-heading text-body-1" style="font-weight: 700; margin: 0;">RTI Act & Transparency</h5>
            <span class="text-caption" style="font-size: 11px;">Admin Services • Updated 2 days ago</span>
          </div>
        </td>
        
        <!-- Status Pill Badge -->
        <td style="padding: 14px 12px; vertical-align: middle; text-align: center; width: 90px;">
          <span class="bg-accent-green text-permanent-white" style="padding: 3px 8px; border-radius: var(--radius-999); font-size: 10px; font-weight: 700; text-transform: uppercase;">Active</span>
        </td>
        
        <!-- Learners counter -->
        <td style="padding: 14px 12px; vertical-align: middle; text-align: right; width: 100px;">
          <div style="display: flex; flex-direction: column;">
            <span class="text-body" style="font-weight: 700; font-size: 13px;">1,240</span>
            <span class="text-caption" style="font-size: 10px;">Enrolled</span>
          </div>
        </td>
        
        <!-- Trigger option menu -->
        <td style="padding: 14px 16px; vertical-align: middle; text-align: center; width: 50px;">
          <span class="material-icons icon-secondary" style="cursor: pointer;">more_vert</span>
        </td>
      </tr>
    </tbody>
  </table>
</div>
```

### 10. Tags & Badge Competency Cloud
```html
<div style="display: flex; gap: 8px; flex-wrap: wrap;">
  <!-- Primary Pill -->
  <span class="bg-primary-50 text-primary bordered-primary" style="padding: 6px 12px; border-radius: var(--radius-999); font-size: 11.5px; font-weight: 700; display: inline-flex; align-items: center; gap: 4px;">
    <span class="material-icons" style="font-size: 14px;">computer</span> Digital Fluency
  </span>
  
  <!-- Secondary Pill -->
  <span class="bg-secondary-50 text-secondary bordered-secondary" style="padding: 6px 12px; border-radius: var(--radius-999); font-size: 11.5px; font-weight: 700; display: inline-flex; align-items: center; gap: 4px;">
    <span class="material-icons" style="font-size: 14px;">psychology</span> Public Policy
  </span>
  
  <!-- Success Pill -->
  <span class="bg-card-success text-success border-accent-success" style="border: 1px solid; padding: 6px 12px; border-radius: var(--radius-999); font-size: 11.5px; font-weight: 700; display: inline-flex; align-items: center; gap: 4px;">
    <span class="material-icons" style="font-size: 14px;">check_circle</span> Core Ethics
  </span>

  <!-- Warning Pill -->
  <span class="bg-card-warning text-warning border-accent-warning" style="border: 1px solid; padding: 6px 12px; border-radius: var(--radius-999); font-size: 11.5px; font-weight: 700; display: inline-flex; align-items: center; gap: 4px;">
    <span class="material-icons" style="font-size: 14px;">campaign</span> Urgent Reform
  </span>
</div>
```

---

## Combining with Typography & Spacing Utilities

These color classes work alongside the existing typography and spacing utilities:

```html
<div class="bg-card bordered p-16">
  <h2 class="text-heading-2 text-heading mb-8">Section Title</h2>
  <p class="text-body-1 text-body mb-16">Description paragraph.</p>
  <a class="text-link text-button-1">Read More →</a>
</div>
```

---

## Quick Reference: Which class for which element?

| HTML Element | Recommended Class | Notes |
|---|---|---|
| `<h1>` - `<h3>` | `.text-heading` | Auto-flips black ↔ white |
| `<h4>` - `<h6>` | `.text-sub-heading` | Slightly lower opacity |
| `<p>` | `.text-body` | Standard body text |
| `<a>` | `.text-link` | Blue in light, white in dark |
| `<label>` | `.text-label` | Form labels |
| `<small>`, `<caption>` | `.text-caption` | Small text |
| `<span class="error">` | `.text-error` | Red in both themes |
| `<mat-icon>` | `.icon-primary` | Flips black ↔ white |
| Card container | `.bg-card .bordered` | Theme-aware card |
| Page background | `.bg-surface-primary` | White ↔ Navy |
| Sidebar | `.bg-surface-secondary` | Light gray ↔ Dark gray |
| Primary button | `.btn-filled-primary` | With hover/disabled states |
| Secondary button | `.btn-filled-secondary` | Orange with states |
| Outline button | `.btn-outlined-primary` | Border only |
