<template>
  <div id="app">
    <Header/>
    <Home/>
  </div>
</template>

<script>
// importando os arquivos
import './styles/global.css';

// importando os componentes
import Header from './components/Header';
import Home from './pages/Home';

export default {
  name: 'App',
  components: {
    Header,
    Home
  }
}
</script>

