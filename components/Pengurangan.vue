<template>
  <div id="app">
      <form  class="text-center" style="margin-top: 5%">
        <h1 class="text-center">Pengurangan</h1>
        <input type="number" v-model.number="angka_3"> -
        <input type="number" v-model.number="angka_4">
    </form>
  <h2 class="text-center">Hasil : {{ angka_3 - angka_4}}</h2>
  </div>
</template>

<script>

export default {
  name: 'pengurangan',
  data: function () {
    return {
      angka_3: null,
      angka_4: null
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
