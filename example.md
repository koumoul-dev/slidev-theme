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

# Default Logo

This slide shows the bottom-right logo (default behavior).

---
layout: section
---

# Section Without Logo

The logo is hidden by default on `section` slides.

---
layout: section
bottom-logo: true
---

# Section With Logo

The `bottom-logo: true` frontmatter forces the logo on this section slide.

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
