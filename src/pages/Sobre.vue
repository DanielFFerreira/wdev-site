<template>
  <main>
    <section class="container">
      <h1>Sobre</h1>

      <div class="about" v-html="about"></div>

    </section>
  </main>
</template>

<script>
  import api from '@/services/api.js'

export default {
  name:'Sobre',
  data() {
    return {
      about: ''
    }
  },
  mounted() {
    api.get('/about.json').then(response => {
      this.about = response.data.about;
    });
  }
}
</script>

<style scoped>
  main {
    align-items: center;
    margin: 0 auto;
  }
  .about {
    margin-bottom: 1.87rem;
    color: var(--color-text-dark);
  }
  @media (min-width: 370px) and (max-width: 700px) {
    main {
      max-width: 390px;
    }
  }
</style>