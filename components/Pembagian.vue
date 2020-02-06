<template>
  <div id="app">
    <form  class="text-center" style="margin-top: 5%">
        <h1 class="text-center">Pembagian</h1>
        <input type="number" v-model.number="angka_5"> /
        <input type="number" v-model.number="angka_6">
    </form>
  <h2 class="text-center">Hasil : {{ angka_5 / angka_6}}</h2>
  </div>
</template>

<script>

export default {
  name: 'Pembagian',
  data: function () {
    return {
      angka_5: null,
      angka_6: null
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
