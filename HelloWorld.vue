<template>
  <div class="container">
        <h1 class="text-center">Kalkulator</h1>
    <form  class="text-center" style="margin-top: 10%">
        <h1 class="text-center">Penjumlahan</h1>
        <input type="number" v-model.number="angka_1"> +
        <input type="number" v-model.number="angka_2">
    </form>
  <h2 class="text-center">Hasil : {{ angka_1 + angka_2}}</h2>

  <form  class="text-center" style="margin-top: 5%">
        <h1 class="text-center">Pengurangan</h1>
        <input type="number" v-model.number="angka_3"> -
        <input type="number" v-model.number="angka_4">
    </form>
  <h2 class="text-center">Hasil : {{ angka_3 - angka_4}}</h2>

  <form  class="text-center" style="margin-top: 5%">
        <h1 class="text-center">Pembagian</h1>
        <input type="number" v-model.number="angka_5"> /
        <input type="number" v-model.number="angka_6">
    </form>
  <h2 class="text-center">Hasil : {{ angka_5 / angka_6}}</h2>

  <form  class="text-center" style="margin-top: 5%">
        <h1 class="text-center">Perkalian</h1>
        <input type="text" v-model.number="angka_7"> *
        <input type="text" v-model.number="angka_8">
    </form>
  <h2 class="text-center">Hasil : {{ angka_7 * angka_8}}</h2>
<!--
    <div class="calculator">
      <div class="prev">{{ previous || '' }} {{ sign }}</div>
      <div class="display">{{ current || '0' }}</div>
      <div @click="clearAll" class="btn operator2 c">C</div>
      <div @click="del" class="btn operator2">🔙</div>
      <div @click="divide" class="btn operator2">÷</div>
      <div @click="append('7')" class="btn">7</div>
      <div @click="append('8')" class="btn">8</div>
      <div @click="append('9')" class="btn">9</div>
      <div @click="times" class="btn operator2">x</div>
      <div @click="append('4')" class="btn">4</div>
      <div @click="append('5')" class="btn">5</div>
      <div @click="append('6')" class="btn">6</div>
      <div @click="minus" class="btn operator2">-</div>
      <div @click="append('1')" class="btn">1</div>
      <div @click="append('2')" class="btn">2</div>
      <div @click="append('3')" class="btn">3</div>
      <div @click="add" class="btn operator2">+</div>
      <div @click="sign" class="btn">±</div>
      <div @click="append('0')" class="btn">0</div>
      <div @click="dot" class="btn">.</div>
      <div @click="equal" class="btn operator2">=</div>
    </div>
-->
 </div>

</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data: function () {
    return { angka_1: null,
      angka_2: null,
      angka_3: null,
      angka_4: null,
      angka_5: null,
      angka_6: null,
      angka_7: null,
      angka_8: null,
      calculator: {
        previous: null,
        current: '',
        operator: null,
        operatorClicked: false,
        sign: '',
        end: false
      }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}

.calculator {
  margin: 0 auto;
  width: 250px;
  height: 450px;
  text-align: center;
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-auto-rows: minmax(30px, auto);
  box-shadow: 5px 10px 8px #888888;
}

.display {
  padding: 10px;
  grid-column:  1 / 5;
  display: flex;
  justify-content: flex-end;
  align-items: center;
  background-color: #333;
  color: #fff;
  text-align: center;
}
.prev {
  grid-column:  1 / 5;
  display: flex;
  justify-content: flex-end;
  align-items: center;
  background-color: #333;
  color: #fff;
  border: 1px solid #eee
}

.c {
  grid-column:  1 / 3;
}

.btn {
  background-color: #f2f2f2;
  border: 1px solid #333;
  display: flex;
  justify-content: center;
  align-items: center;
}
.btn:hover { background-color: rgb(33.8%, 86.6%, 50.5%); cursor: pointer; }

.operator { background-color:rgb(34.7%, 53.3%, 84.7%) }
.operator:hover { background-color: rgb(21.9%, 37.6%, 64%); cursor: pointer; }
.operator2 { background-color: rgb(32.1%, 50.5%, 81.6%) }
.operator2:hover { background-color: rgb(21.9%, 37.6%, 64%); cursor: pointer; }

</style>
