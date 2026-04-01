<template>
  <div v-if="isPrimaryBg" class="bg-primary-overlay" />
  <div v-if="showLogo" class="global-logo">
    <img :src="logoCircleUrl" alt="Koumoul" />
  </div>
</template>

<script setup lang="ts">
import { computed } from 'vue'
import { useSlideContext } from '@slidev/client'
import logoCircleUrl from './public/logo-circle.png'

const { $frontmatter, $nav } = useSlideContext()

const isPrimaryBg = computed(() => $frontmatter.background === 'primary')

const showLogo = computed(() => {
  const val = $frontmatter['bottom-logo']
  if (val !== undefined) {
    return val !== false && val !== 'false'
  }
  const layout = $nav.value.currentLayout
  return layout !== 'section' && layout !== 'cover'
})
</script>

<style scoped>
.bg-primary-overlay {
  position: absolute;
  inset: 0;
  background: var(--slidev-theme-primary);
  z-index: -1;
}

.global-logo {
  position: fixed;
  right: 1.5rem;
  bottom: 1rem;
  z-index: 10;
}

.global-logo img {
  height: 3rem;
  opacity: 0.8;
}
</style>

<style>
.slidev-page:has(.bg-primary-overlay) .slidev-layout {
  background: transparent;
  color: white;
}

.slidev-page:has(.bg-primary-overlay) .slidev-layout h1,
.slidev-page:has(.bg-primary-overlay) .slidev-layout h2,
.slidev-page:has(.bg-primary-overlay) .slidev-layout h3,
.slidev-page:has(.bg-primary-overlay) .slidev-layout h4 {
  color: white;
}

.slidev-page:has(.bg-primary-overlay) .slidev-layout a {
  color: white;
}

.slidev-page:has(.bg-primary-overlay) .slidev-layout a:hover {
  color: var(--slidev-theme-primary-light);
}

.slidev-page:has(.bg-primary-overlay) .slidev-layout code {
  background: rgba(255, 255, 255, 0.2);
  color: white;
}
</style>
