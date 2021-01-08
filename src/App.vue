<template>
  <div id="app">
    <Header/>
    <Home/>
    <Footer/>
  </div>
</template>

<script>
// importando os arquivos
import './styles/global.css';

// importando os componentes
import Header from './components/Header';
import Home from './pages/Home';
import Footer from './components/Footer';

export default {
  name: 'App',
  components: {
    Header,
    Home,
    Footer
  }
}
</script>

