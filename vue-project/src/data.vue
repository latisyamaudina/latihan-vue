
<template>
    <div>
      <h1>Formulir</h1>
      <form @submit.prevent="submitorm">
        <label for="">Nama :  &nbsp; &nbsp; &nbsp;</label>
        <input type="text" name="nama" id="nama" v-model="data.nama">
        <br>
        <label for="">Kelas : &nbsp; &nbsp; &nbsp; &nbsp;</label>
        <input type="text" name="kelas" id="kelas" v-model="data.kelas">
        <br>
        <label for="">Alamat :&nbsp; &nbsp; &nbsp;</label>
        <input type="text" name="alamat" id="alamat" v-model="data.alamat"> 
        <br>
        <label for="">Nilai MTK : </label>
        <input type="number" name="mtk" id="mtk" v-model="data.mtk">
        <br>
        <label for="">Nilai IPA : &nbsp; &nbsp;</label>
        <input type="number" name="ipa" id="ipa" v-model="data.ipa">
        <br>
        <label for="">Nilai B.indonesia : </label>
        <input type="number" name="bindo" id="bindo" v-model="data.bindo">
        <br> 
        <br>
        <button type="submit">Simpan</button>
        <br>
        <br>
        <br>
      </form>
      <div v-if="showResult">
        Nama : {{ name }} <br>
        Kelas : {{ kelas }} <br>
        Alamat : {{ alamat }} <br>
        Nilai Mtk : {{ mtk }} <br>
        Nilai Ipa : {{ ipa }} <br>
        Nilai Bindo : {{ bindo }} <br>
        Total Nilai : {{ mtk + ipa + bindo }} <br>
        Status : {{ mtk + ipa + bindo >= 240 ? 'Lulus' : 'Tidak Lulus' }}
  
      </div>
    </div>
  </template>
  
  <script>
  
  
  import { ref } from 'vue';
  export default {
    name: 'MyComponent',
    data() {
      return {
         data : 
          {
            name: '', 
            kelas: '',
            alamat: '',
            mtk: '',
            ipa: '',
            bindo: ''
  
          },
        showResult: ref(false),
            name: '', 
            kelas: '',
            alamat: '',
            mtk: '',
            ipa: '',
            bindo: '',
            total: 0
        };
      },
  
        methods: {
          submitorm() {
        this.name = this.data.nama; 
        this.kelas = this.data.kelas;
        this.alamat = this.data.alamat;
        this.mtk = this.data.mtk;
        this.ipa = this.data.ipa;
        this.bindo = this.data.bindo;
        this.showResult = true;
           
        }
       }
      }
     
       
  </script>
  
  <style>
  h1 {
    color: rgb(251, 251, 251);
  }
  
  .error-message{
    color:red;
    margin-top: 5px
  }
  
  .is-invalid {
    border-color:red;
  }
  </style>