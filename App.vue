<template>
  <div>
    <penjumlahan/>
    <pengurangan/>
    <perkalian/>
    <pembagian/>
  </div>
</template>

<script>
import Penjumlahan from './components/Penjumlahan.vue'
import Pengurangan from './components/Pengurangan.vue'
import Perkalian from './components/Perkalian.vue'
import Pembagian from './components/Pembagian.vue'

export default {
  name: 'app',
  components: {
    Penjumlahan,
    Pengurangan,
    Perkalian,
    Pembagian
  },
  data () {
    return ({
      message: 'Kalkulator'
    })
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
