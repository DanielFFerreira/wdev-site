<template>
  <footer>
    <a v-for="(socialLink,index) in socialLinks" :key="index" class="socialLink" :href="socialLink.link" target="_blank">
      <img :src="socialLink.icon" :alt="socialLink.label" :title="socialLink.label">
    </a>
  </footer>
</template>

<script>
import api from '@/services/api.js';

export default {
  name: 'Footer',
  data() {
    return {
      socialLinks: []
    }
  },
  mounted() {
    api.get('/social-links.json').then(response => {
      this.socialLinks = response.data;
    });
  }
}
</script>

<style scoped>

  .socialLink {
    border: 2px solid var(--color-text-light);
    display: flex;
    align-items: center;
    justify-content: center;
    border-radius: 50%;
    width: 2.5rem;
    height: 2.5rem;
    margin: 0 10px;
  }
  .socialLink img {
    width: 1.25rem;
  }
</style>