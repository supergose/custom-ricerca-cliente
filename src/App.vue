<template>
  <div id="app">
    <RicercaCliente msg="Ricerca"/>
  </div>
</template>

<script>
import RicercaCliente from './components/RicercaCliente.vue'

export default {
  name: 'app',
  components: {
    RicercaCliente
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
