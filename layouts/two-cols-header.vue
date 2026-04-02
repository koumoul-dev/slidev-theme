<template>
  <div class="slidev-layout two-cols-header w-full h-full">
    <div class="col-header" :class="{ 'bg-primary': headerIsPrimary }">
      <slot />
    </div>
    <div class="col-left" :class="{ 'card-primary': leftIsPrimary }">
      <slot name="left" />
    </div>
    <div class="col-right" :class="{ 'card-primary': rightIsPrimary }">
      <slot name="right" />
    </div>
    <div class="col-bottom">
      <slot name="bottom" />
    </div>
  </div>
</template>

<script setup>
import { computed } from 'vue'
import { useSlideContext } from '@slidev/client'

const { $frontmatter } = useSlideContext()
const headerIsPrimary = computed(() => $frontmatter['header-bg'] === 'primary')
const leftIsPrimary = computed(() => $frontmatter['left-bg'] === 'primary')
const rightIsPrimary = computed(() => $frontmatter['right-bg'] === 'primary')
</script>
