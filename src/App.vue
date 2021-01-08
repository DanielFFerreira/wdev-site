<template>
  <div id="app">
    <Header/>
    <Footer/>
  </div>
</template>

<script>
// importando os arquivos
import './styles/global.css';

// importando os componentes
import Header from './components/Header';
import Footer from './components/Footer';

export default {
  name: 'App',
  components: {
    Header,
    Footer
  }
}
</script>

