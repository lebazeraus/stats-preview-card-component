<template>
  <h2 :class="$style.root">
    <slot/>
  </h2>
</template>

<script>
export default {
  name: 'ComponentH2'
}
</script>

<style module>
.root {
  color: var(--white);
  font-size: 1.5rem;
  margin: 0;
}
</style>
