<template>
  <header>
    <nav class="nav-container">
      <!-- Logo -->
      <a href="/"><img src="../assets/images/wdev.svg" alt="logo wdev" id="logo"></a>

      <!-- Menu navegação -->
      <img v-on:click="openMenu" src="../assets/images/menu.svg" alt="menu" id="menu-button">

      <!-- Menu overlay -->
      <div id="menu-overlay" v-if="menuActive"></div>

      <!-- Menu listas -->
      <div id="menu-items" :class="{active:menuActive}">

        <img v-on:click="closeMenu" src="../assets/images/close.svg" alt="menu fechar" id="menu-close">

        <img src="../assets/images/wdev.svg" alt="logo wdev" id="menu-logo">

        <ul>
          <li><a href="/">Home</a></li>
          <li><a href="/videos">Vídeos</a></li>
          <li><a href="/sobre">Sobre</a></li>
          <li><a href="/contato">Contato</a></li>
        </ul>
      </div>
    </nav>
  </header>
</template>

<script>
export default {
  name: 'Header',
  data() {
    return {
      menuActive: true
    }
  },
  methods: {
    openMenu: function() {
      this.menuActive = true;
    },
    closeMenu: function() {
      this.menuActive = false;
    }
  }
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
  nav {
    display: flex;
    justify-content: space-between;
    align-content: center;
    height: 60px;
    align-items: center;
  }
  #logo {
    width: 8.12rem;
  }

  #menu-button {
    width: 30px;
  }
  #menu-close {
    width: 30px;
    position: absolute;
    top: 10px;
    left: 10px;
  }

  #menu-overlay {
    position: fixed;
    top: 0;
    left: 0;
    width: 40%;
    height: 100vh;
    background: var(--color-background-overlay);
    opacity: 0.8;
  }
  #menu-logo {
    width: 6.87rem;
    margin-top: 3.87rem;
    margin-bottom: 10px;
  }
  #menu-items {
    position: fixed;
    top: 0;
    right: 0;
    background: var(--color-background-nav);
    width: 60%;
    height: 100vh;
    display: none;
    flex-direction: column;
    justify-content: flex-start;
    align-items: center;
  }
  #menu-items.active {
    display: flex;
  }

  ul {
    list-style: none;
    text-align: center;
  }
  ul li {
    margin: 1.25rem 0;
  }
  ul li a {
    color: var(--color-text-light);
  }

  @media (min-width: 700px) {
    #menu-button,
    #menu-logo,
    #menu-overlay,
    #menu-close {
      display: none;
    }
    #menu-items {
      display: flex;
      position: static;
      height: 60px;
      width: auto;
    }
    ul {
      display: flex;
      height: 60px;
      align-items: center;
    }
    ul li {
      margin: 0;
      margin-left: 25px;
    }

  }

</style>