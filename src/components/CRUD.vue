<template>
  <div id="CRUD">
      <div class="Label">
          <h2>CRUD</h2>
      </div>
      <br>
<div class="container">

    <div class="inputan">
        <div class="card mb-3" v-for="(data,index) in allData" :key="index">
            <div class="card-body">
                <div class="employee-form">
                    <h2><b>Detail Tugas ke-{{index+1}}</b></h2>
                    <hr>
                    <input type="text" class="form1" placeholder="Nama Tugas" v-model="data.namaTugas">
                    <input type="text" class="form1" placeholder="Mata Kuliah" v-model="data.mataKuliah">
                    <input type="date" class="form1" placeholder="Deadline" v-model="data.deadline">
                    <br>
                    <textarea class="form2" cols="75" rows="10" placeholder="Deskripsi" v-model="data.deskripsi"></textarea>
                    <div class="aa">
                        <button class="btnTambah" mt-5 mb-5 @click="tambahkan">Tambahkan Tugas</button>
                    </div>
                    <br>
                    <a class="btn btn-primary" data-toggle="collapse" href="#collapseExample" role="button" aria-expanded="false" aria-controls="collapseExample">
                        Detail
                    </a>
                </div>
                <br>
                <div class="collapse" id="collapseExample">
                    <div class="card-body-detail">
                        <span class="float-right" style="cursor: pointer" data-toggle="collapse" href="#collapseExample">
                            <button class="btnHapus" @click="hapus(index)">hapus</button>
                        </span>
                        <h2>Detail Tugas ke-{{index+1}}</h2>
                        <hr>
                        <div class="detail">
                            <h4>Nama Tugas  : {{data.namaTugas}}</h4>
                            <h4>Mata Kuliah : {{data.mataKuliah}}</h4>
                            <h4>Deadline    : {{data.deadline}}</h4>
                            <h4>Deskripsi   : {{data.deskripsi}}</h4>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</div>
</div>
</template>

<script>

export default {
  name: 'CRUD',
  components: {

  },
  data () {
    return {
      allData: [
        {
          namaTugas: '',
          mataKuliah: '',
          deadline: '',
          deskripsi: ''
        }
      ]
    }
  },
  methods: {
    tambahkan () {
      this.allData.push({
        namaTugas: '',
        mataKuliah: '',
        deadline: '',
        deskripsi: ''
      })
    },
    hapus (index) {
      this.allData.splice(index, 1)
    }
  }
}
</script>

<style>
.employee-form{
    position: sticky;
    padding: 10px;
    background-color: yellowgreen;
    border: 2px solid #4CAF50;
    border-radius: 5px;
}
.form1{
    margin-right: 5px;
    margin-bottom: 5px;
    padding: 10px;
    border-radius: 5px;
    background-color: whitesmoke;
    border: 2px solid black;
}
.form2{
    margin-right: 5px;
    padding: 10px;
    border-radius: 5px;
    background-color: whitesmoke;
    border: 2px solid black;
}
.btnTambah{
    padding: 10px;
    border-radius: 25px;
    background-color: #cae8ca;
    border: 2px solid #4CAF50;
}
.btnHapus{
    padding: 10px;
    border-radius: 5px;
    background-color: red;
    border: 2px solid black;
}
.card-body-detail{
    text-align: left;
    background: greenyellow;
    border: 2px solid #4CAF50;
    padding: 10px;
    border-radius: 5px;
}
</style>
