<template>
  <div class="lista">
    <h4>{{ titulo }}</h4>

    <ul class="list-group">
        <li class="list-group-item" v-for="(item, i) in tech" v-bind:key="i">
            <a v-bind:href="item.url">{{ item.texto }}</a>
        </li>
    </ul>
  </div>
</template>

<script>
export default {
    name: "Lista",
    props: {
        titulo: String,
        tech: Array
    }
};
</script>

<style scoped>
h4 {
    color: red;
    padding-left: 10px;
}
ul {
  list-style-type: none;
  padding: 0;
  margin-bottom: 20px;
}
li {
  display: block;
  margin: 0 10px;
}
</style>