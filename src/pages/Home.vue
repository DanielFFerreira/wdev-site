<template>
  <main>
    <div class="text-top">Projeto para procurar vídeos</div>

    <a href="https://github.com/DanielFreitasFerreira" target="_blank">
      <img src="../assets/images/gitHub.png" alt="icon github">
    </a>

    <div class="text-bottom">github.com/DanielFreitasFerreira</div>
  </main>
</template>

<script>
export default {
  name: 'Home'
}
</script>

<style scoped>
  main {
    background: var(--color-background-home);
    justify-content: center;
    align-items: center;
  }
  img {
    width: 12.75rem;
  }

  .text-top {
    color: var(--color-text-light);
    font-size: 1.37rem;
    margin-bottom: 1.25rem;
  }
  .text-bottom {
    color: var(--color-text-light);
    font-size: 1.12rem;
    margin-top: 1.25rem;
  }

  @media (min-width: 700px) {
    img {
      width: 15rem;
    }
  }
</style>