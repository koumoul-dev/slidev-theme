<template>
  <div v-if="showLogo" class="global-logo">
    <img src="/logo-circle.png" alt="Koumoul" />
  </div>
</template>

<script setup>
import { computed } from 'vue'
import { useSlideContext } from '@slidev/client'

const { $frontmatter } = useSlideContext()

const showLogo = computed(() => {
  if ($frontmatter['bottom-logo'] !== undefined) {
    return !!$frontmatter['bottom-logo']
  }
  const layout = $frontmatter.layout || 'default'
  return layout !== 'section'
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
