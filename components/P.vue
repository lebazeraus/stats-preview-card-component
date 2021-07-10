<template>
  <p v-if="$props.text" :class="$style.root" v-html="$props.text"></p>
  <p v-else :class="$style.root"><slot/></p>
</template>

<script>

export default {
  name: 'ComponentP',
  props: {
    text: { type: String }
  }
}
</script>

<style module>
.root {
  color: var(--gray);
  font-size: 1em;
  margin: 0;
}

.root a {
  color: var(--accent-color);
  text-decoration-line: none;
}
</style>
