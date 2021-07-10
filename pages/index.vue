<template>
  <div :class="$style.root">
    <Card/>
  </div>
</template>

<script>
export default {
  name: 'PageIndex'
}
</script>

<style module>
@media screen and (min-width: 60em) {
  .root {
    padding: 0 1.5rem;
  }
}
</style>
