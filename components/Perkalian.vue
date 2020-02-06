<template>
  <div id="app">
    <form  class="text-center" style="margin-top: 5%">
        <h1 class="text-center">Perkalian</h1>
        <input type="text" v-model.number="angka_7"> *
        <input type="text" v-model.number="angka_8">
    </form>
  <h2 class="text-center">Hasil : {{ angka_7 * angka_8}}</h2>
  </div>
</template>

<script>

export default {
  name: 'Perkalian',
  data: function () {
    return {
      angka_7: null,
      angka_8: null
    }
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
