<template>
  <header>
    <nav class="nav-container">
      <a href="/">
        <img alt="logo" id="logo" src="../assets/images/wdev.svg">
      </a>
      <!-- Adicionar botão menu -->
      <img id="menu-logo" src="../assets/images/menu.svg" alt="menu">
    </nav>
  </header>
</template>

<script>
export default {
  name: 'Header'
}
</script>

<style scoped>
  header {
    background: var(--color-background-nav);
    width: 100%;
    height: 60px;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  #logo {
    width: 8.12rem;
  }
  #menu-logo {
    width: 1.87rem;
  }
  nav {
    display: flex;
    justify-content: space-between;
  }
</style>