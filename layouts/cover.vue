<script setup>
import logoUrl from '../public/logo.png'
</script>

<template>
  <div class="slidev-layout cover">
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
  background: var(--slidev-theme-primary);
  position: relative;
  z-index: 1;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.3);
}

.cover-footer {
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 1.5rem;
  background: var(--slidev-theme-background);
}

.cover-logo {
  height: 3rem;
}
</style>
