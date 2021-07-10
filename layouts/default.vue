<template>
  <div :class="$style.root">
    <nuxt/>
    <footer :class="$style.root__footer">
      <P text="Foto de <a href='https://www.pexels.com/es-es/@fauxels?utm_content=attributionCopyText&utm_medium=referral&utm_source=pexels' target='_blank'>fauxels</a> en <a href='https://www.pexels.com/es-es/foto/foto-de-personas-sentadas-cerca-de-la-mesa-de-madera-3182764/?utm_content=attributionCopyText&utm_medium=referral&utm_source=pexels' target='_blank'>Pexels</a>"/>
      <P text="Diseño <a href='https://www.frontendmentor.io/challenges/stats-preview-card-component-8JqbgoU62' target='_blank'> Frontend Mentor</a>"/>
    </footer>
  </div>
</template>

<script>
export default {
  name: 'LayoutDefault'
}
</script>

<style module>
.root {
  padding-bottom: 1.5rem;
}

.root__footer {
  display: flex;
  flex-flow: wrap;
  font-size: 12px;
  gap: 1rem;
  justify-content: center;
  padding: 1.5rem 1.5rem 0;
  text-align: center;
}
</style>
