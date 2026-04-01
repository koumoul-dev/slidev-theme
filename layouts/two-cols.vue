<template>
  <div class="slidev-layout two-cols">
    <div class="col-left" :class="{ 'bg-primary': leftIsPrimary }">
      <slot />
    </div>
    <div class="col-right" :class="{ 'bg-primary': rightIsPrimary }">
      <slot name="right" />
    </div>
  </div>
</template>

<script setup>
import { computed } from 'vue'
import { useSlideContext } from '@slidev/client'

const { $frontmatter } = useSlideContext()
const leftIsPrimary = computed(() => $frontmatter['left-bg'] === 'primary')
const rightIsPrimary = computed(() => $frontmatter['right-bg'] === 'primary')
</script>
