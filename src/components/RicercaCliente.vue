<template>
  <div class="ricerca-cliente">
    <h2>{{ msg }}</h2>
    <ul>
      <li v-for="item in todos" :key="item.id">{{ item.title }}</li>
    </ul>
  </div>
</template>

<script>
/* eslint-disable */
import { ToDoService } from "@supergose/jsonplaceholder-services";

export default {
  name: 'RicercaCliente',
  props: {
    msg: String
  },
  mounted() {
    this.getTodos();
  },
  data() {
    return {
      todos: null
    };
  },
  methods: {
    async getTodos() {
      let response = await ToDoService.getTodos();
      this.todos = response.data;
    }
  }
}
</script>

<style scoped>
.ricerca-cliente {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  border-radius: 25px;
  background-color: rgb(240, 240, 240);
  border: 1px solid rgb(214, 214, 214);
  color: #2c3e50;
  padding: 20px;
}

h2 {
  margin: 5px;
  text-align: left;
}

ul {
  max-height: 150px;
  overflow-y: scroll;
}
</style>
