<script setup>
defineProps({
  label: { type: String, required: true },
  value: { type: [String, Number], required: true },
  variant: {
    type: String,
    default: 'flat',
    validator: (v) => ['flat', 'card', 'card-primary'].includes(v)
  }
})
</script>

<template>
  <div class="kpi" :class="variant">
    <div class="kpi-icon"><slot /></div>
    <div class="kpi-value">{{ value }}</div>
    <div class="kpi-label">{{ label }}</div>
  </div>
</template>

<style scoped>
.kpi {
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
  gap: 0.125rem;
  padding: 0.25rem 0.5rem;
}

.kpi.card,
.kpi.card-primary {
  margin: 0.25rem 0;
  padding: 0.6rem 0.75rem;
  border-radius: 0.6rem;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.3);
}

.kpi.card {
  background: white;
  color: var(--slidev-theme-text);
}

.kpi.card .kpi-icon {
  color: var(--slidev-theme-primary);
}

.kpi.card-primary {
  background: var(--slidev-theme-primary);
  color: white;
}

.kpi.card-primary .kpi-icon {
  color: white;
}

.kpi-icon {
  font-size: 1.75rem;
  line-height: 1;
  color: var(--slidev-theme-primary);
  margin-bottom: 0.125rem;
}

.kpi-value {
  font-size: 2rem;
  font-weight: 700;
  line-height: 1.1;
  color: inherit;
}

.kpi-label {
  font-size: 0.8rem;
  opacity: 0.75;
  color: inherit;
}
</style>
