<template>
  <label :class="$style.root">
    <slot/>
  </label>
</template>

<script>
export default {
  name: 'ComponentLabel'
}
</script>

<style module>
.root {
  color: var(--gray);
  font-size: .75rem;
  letter-spacing: .075rem;
}
</style>
