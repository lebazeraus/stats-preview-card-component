<template>
  <h1 :class="classes" v-html="text"></h1>
</template>

<script>
import { computed, wrapProperty } from '@nuxtjs/composition-api'
const useStyle = wrapProperty('$style', false)

export default {
  name: 'ComponentH1',
  props: {
    text: { type: String },
    marginBottom: { type: Boolean }
  },
  setup(props) {
    const $style = useStyle()
    const classes = computed({
      set: () => {},
      get: () => {
        return {
          [$style.root]: true,
          [$style['root--margin-bottom']]: props.marginBottom,
        }
      },
    })

    return {
      classes
    }
  }
}
</script>

<style module>
.root {
  color: var(--white);
  font-size: 1.75rem;
  line-height: 2rem;
  margin: 0;
}
.root b[accent-color] {
  color: var(--accent-color)
}
.root--margin-bottom {
  margin-bottom: 1.5rem;
}

@media screen and (min-width: 60rem) {
  .root {
    font-size: 2rem;
    line-height: 2.5rem;
  }
}
</style>
