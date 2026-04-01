<script setup>
import logoUrl from '../public/logo-slogan-white.png'
</script>

<template>
  <div class="slidev-layout cover bg-primary">
    <div class="cover-content">
      <slot />
    </div>
    <div class="cover-footer">
      <img :src="logoUrl" class="cover-logo" alt="Koumoul" />
    </div>
  </div>
</template>

<style scoped>
.cover-content {
  flex: 1;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  width: 100%;
  text-align: center;
}

.cover-footer {
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 1.5rem;
}

.cover-logo {
  height: 3rem;
}
</style>
