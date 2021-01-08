<template>
  <main>
    <section class="container">
      <h1>Contato</h1>

      <section class="contacts" v-for="(contact,index) in contacts" :key="index">
        <div class="contact">
          <div class="contact-title">{{ contact.title }}</div>

          <a href=""></a>
        </div>
      </section>

    </section>
  </main>
</template>

<script>
  import api from '@/services/api.js'

export default {
  name:'Contato',
  data() {
    return {
      contacts: []
    }
  },
  mounted() {
    api.get('/contacts.json').then(response => {
      this.contacts = response.data;
    });
  }
}
</script>

<style scoped>
  main {
    align-items: center;
    margin: 0 auto;
  }
  .contacts {
    margin-bottom: 1.87rem;
    color: var(--color-text-dark);
  }
  @media (min-width: 370px) and (max-width: 700px) {
    main {
      max-width: 390px;
    }
  }
</style>