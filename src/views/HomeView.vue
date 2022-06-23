<template>
  <div class="container">
    <h1>Tienda 32 Bits</h1>
    <h2>Lista de juegos</h2>
    <table>
      <thead>
      <tr>
        <th>Código</th>
        <th>Nombre</th>
        <th>Stock</th>
        <th>Precio</th>
      </tr>
      </thead>
      <tbody v-for="game in games" :key="game.codigo">
      <tr :style="{color: game.color}">
        <td>{{ game.codigo }}</td>
        <td>{{ game.nombre }}</td>
        <td>{{ game.stock }}</td>
        <td>{{ game.precio }}</td>
      </tr>
      </tbody>
    </table>

  </div>
</template>

<script>
// @ is an alias to /src

import {mapState} from 'vuex'

export default {
  name: 'HomeView',
  computed: {
    ...mapState(['games'])
  },
}
</script>

<style scoped>
.container {
  display: grid;
  grid-template-columns: 800px;
  justify-content: center;
  width: 70%;
  margin: 0 auto;
}

td{
  border:2px solid black;
}

th{
  border:2px solid black;
}

</style>