<template>
  <div class="ricerca-cliente">
    <h2>{{ msg }}</h2>
  </div>
</template>

<script>
export default {
  name: 'RicercaCliente',
  props: {
    msg: String
  }
}
</script>

<style scoped>
.ricerca-cliente {
  border: 1px solid gray;
  color: navy;
}

h2 {
  margin: 5px;
  text-align: left;
}
</style>
