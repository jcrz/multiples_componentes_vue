<template>
  <div id="app">
    <Header titulo="Tareas por aprender" />
    <div class="contenedor">
      <Lista
        titulo="Tech"
        v-bind:tech="tech"
      />
      <Lista
        titulo="Financial"
        v-bind:tech="Financial"
      />
    </div>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Lista from "./components/Lista.vue";

export default {
  name: "App",
  components: {
    Header,
    Lista
  },
  data: function(){
    return {
      tech: [
        { texto: 'HTML', url: 'https://www.google.com' },
        { texto: 'CSS', url: 'https://www.google.com' },
        { texto: 'Vue', url: 'https://www.google.com' },
        { texto: 'Firebase', url: 'https://www.google.com' }
      ],
      Financial: [
        { texto: 'Investing', url: 'https://www.google.com' },
        { texto: 'Budgeting', url: 'https://www.google.com' },
        { texto: 'Balancing a checkbook', url: 'https://www.google.com' }
      ]
    }
  }
};
</script>

<style>
.contenedor {
  width: 500px;
  margin: 50px auto;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
</style>
