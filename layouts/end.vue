<script setup>
import logoSloganWhiteUrl from '../public/logo-slogan-white.png'
</script>

<template>
  <div class="slidev-layout end">
    <div class="end-content">
      <slot />
    </div>
    <img :src="logoSloganWhiteUrl" class="end-logo" alt="Koumoul" />
  </div>
</template>

<style scoped>
.end-logo {
  height: 4rem;
  margin-top: 2rem;
}
</style>
