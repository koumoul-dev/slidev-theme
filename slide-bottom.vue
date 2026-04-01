<template>
  <div v-if="showLogo" class="global-logo">
    <img :src="logoCircleUrl" alt="Koumoul" />
  </div>
</template>

<script setup lang="ts">
import { computed } from 'vue'
import { useSlideContext } from '@slidev/client'
import logoCircleUrl from './public/logo-circle.png'

const { $frontmatter, $nav } = useSlideContext()
const context = useSlideContext()

const showLogo = computed(() => {
  // console.log($nav.nav.currentLayout)
  const val = $frontmatter['bottom-logo']
  if (val !== undefined) {
    return val !== false && val !== 'false'
  }
  const layout = $nav.value.currentLayout
  return layout !== 'section' && layout !== 'cover' && layout !== 'end'
})
</script>

<style scoped>
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
