<script setup>
import logoSloganWhiteUrl from '../public/logo-slogan-white.png'
</script>

<template>
  <div class="slidev-layout cover">
    <img :src="logoSloganWhiteUrl" class="cover-logo" alt="Koumoul" />
    <slot />
  </div>
</template>

<style scoped>
.cover-logo {
  height: 4rem;
  margin-bottom: 2rem;
}
</style>
