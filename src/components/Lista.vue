<template>
  <div>
    <table class="table table-borderless shadow-sm mt-3">
      <tbody>
        <tr v-for="juego in listaJuegos"  :key="juego.codigo" :class="bgColor(juego.color)">
          <td>{{juego.codigo}}</td>
          <td>{{juego.nombre}}</td>
          <td>{{juego.stock}}</td>
          <td>{{juego.precio}}</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
  export default {
    name: 'Lista',
    props: {
      listaJuegos: Array
    },
    methods: {
      bgColor(color) {
        if (color == 'blue') {
          return 'table-primary'
        } else if (color == 'green') {
          return 'table-success'
        } else if (color == 'red') {
          return 'table-danger'
        } else if (color == 'yellow') {
          return 'table-warning'
        }
      }
    }
  }
</script>

<style scoped>

</style>
