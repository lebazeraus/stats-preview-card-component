<template>
  <div :class="$style.root">
    <div :class="$style.root__cover"></div>
    <section :class="$style.root__info">
      <H1 :text="title" marginBottom/>
      <P> {{ description }}</P>
      
      <div :class="$style.root__info__datas">
        <div v-for="($, i) in info.datas" :key="i">
          <H2> {{ $.title }} </H2>
          <Label> {{ $.label }} </Label>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
import { ref } from "@nuxtjs/composition-api";

export default {
  name: 'ComponentCard',
  setup() {
    const title = ref('Obtenga <b accent-color>información</b> que ayude a su negocio a crecer.')
    const description = ref('Descubra las ventajas de la analítica de datos y tome decisiones más acertadas sobre los ingresos, la experiencia del cliente y la eficiencia general.')
    const info = ref({
      datas: [
        { title: '10k+', label: 'EMPRESAS' },
        { title: '314', label: 'PLANTILLAS' },
        { title: '12M+', label: 'CONSULTAS' }
      ]
    })

    return {
      description,
      info,
      title
    }
  }
}
</script>

<style module>
.root {
  overflow: hidden;
}
.root__cover {
  background-blend-mode: multiply;
  background-color: var(--accent-color);
  background-image: url(/images/image-header-mobile.jpg);
  background-position-x: right;
  background-position-y: top;
  background-repeat: no-repeat;
  background-size: cover;
  display: block;
  font-size: 0;
  min-height: 15rem;
  position: relative;
}
.root__cover:after {
  bottom: 0;
  background-color: rgba(var(--accent-color-rgb), 24%);
  content: "";
  left: 0;
  position: absolute;
  right: 0;
  top: 0;
}

.root__info {
  background-color: var(--secondary-color);
  padding: 3em 1.5rem;
  text-align: center;
}

.root__info__datas {
  display: grid;
  gap: 1.5rem;
  margin-top: 1.5rem;
}


@media screen and (min-width: 22.375rem) {
  .root {
    border-radius: .5rem;
    margin: 1.5rem auto;
    max-width: 20rem;
  }
}

@media screen and (min-width: 60rem) {
  .root {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    max-width: 67.5rem;
  }
  .root__info,
  .root__cover {
    grid-row: 1;
  }
  .root__info {
    grid-column: 1;
    text-align: left;
    padding: 4rem 6rem 4rem 3.5rem;
  }
  .root__info__datas {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    margin-top: 4rem;
  }
  .root__cover {
    grid-column: 2;
  }
}
</style>
