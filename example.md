---
theme: ./
---

# My Presentation Title

A subtitle for your talk

---

# About This Talk

This presentation demonstrates the features of the **Slidev theme**.

- Bullet points with nested items
  - Sub-item one
  - Sub-item two
- Clean typography
- Responsive layouts

---

# Key Principles

1. Simple and elegant design
2. Developer-friendly workflow
3. Rich feature set
   - Code highlighting
   - Multiple layouts

---
layout: section
---

# Section Break

---
layout: two-cols
---

# Left Column

Content on the left side of a two-column layout.

- First point
- Second point
- Third point

::right::

# Right Column

Content on the right side of a two-column layout.

- Another point
- Yet another point
- One more point

---
layout: two-cols
left-bg: primary
---

# Primary Left

This column has a primary background with white text and shadow.

- Styled automatically
- Independent from right column

::right::

# Normal Right

This column keeps the default styling.

- Standard text color
- Standard background

---
layout: center
---

# Centered Content

**Vue.js** · **Slidev** · **Markdown** · **Vite**

---

# Code Example

```javascript
import { ref, computed } from 'vue'

const count = ref(0)
const doubled = computed(() => count.value * 2)

console.log(`Count: ${count.value}, Doubled: ${doubled.value}`)
```

---

# Table Example

| Feature | Status |
|---------|--------|
| Slide layouts | Supported |
| Code highlighting | Supported |
| Dark mode | Supported |

---
background: primary
---

# Primary Background

This slide uses `background: primary` to get the primary color background with white text, without changing the layout.

- Works with any layout
- Automatically switches text to white

---
bottom-logo: false
---

# Slide Without Logo

The `bottom-logo: false` frontmatter hides the logo on this slide.

---
layout: end
---

# Thank You!

Questions? Contact us at hello@test.com
