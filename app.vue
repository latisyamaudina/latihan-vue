<script setup>
import { ref } from 'vue'

const msg = "Hallo world"
let headname = "<h1>Nama Saya Latisya</h1>"
let number = 1;
let ok = "NO";
let seen = true;

//split reverse message 
let message = ref ("Haii Vue JS")
function balikkanpesan() {
  message.value = message.value.split('').reverse().join('');
}

//pengulangan
let todos = [
  { teks : 'Belajar JavaScript' },
  { teks : 'Belajar Vue' },
  { teks : 'Buat Proyek Keren' }
]

//input
let pesan = ref("Haii Vue");

//data siswa
let data = [
  { nama: 'Latisya', kelas: 'RPL 1', jurusan: 'RPL'},
  { nama: 'Leyla', kelas: 'RPL 2', jurusan: 'RPL'},
  { nama: 'Shadrina', kelas: 'RPL 1', jurusan: 'RPL'},
  { nama: 'Asti', kelas: 'RPL 1', jurusan: 'RPL'},
  { nama: 'Fitri', kelas: 'RPL 1', jurusan: 'RPL'}
  
]


const rawHtml = "<li>Daftar 1</li>"
const link = "YouTube.com"
const objectOfAttrs = {
  id: 'container',
  class: 'wrapper'
}
let  a = 10
let b = 5
let c = a + b
</script>

<template>
  <div id="app">
    <span>{{ msg }}</span><br>
    <span v-html="rawHtml"></span><br>
    <span style="color: green">Ini Warna Hijau</span><br>
    <span v-html=" headname"></span>
    <button :disabled="isButtonDisabled">Button</button><br>
    <a v-bind:href="url"> YouTube.com </a><br>
    bil1 = {{ a }}<br>
    bil2 = {{ b }}<br>
    hasil = bil1 + bil2 = {{ c }}<br>
    {{ number + 1 }} <br>
    {{ ok ? 'YES' : 'NO' }} <br>

    <!--direktif-->
    <p >{{ message }}</p>
    <button v-on:click="balikkanpesan">Balikkan Pesan</button><br>

    <!--for-->
    <br>pengulangan
    <ol>
      <li v-for = "todo in todos">
        {{ todo.teks }}
      </li>
    </ol>

    <!--input-->
    <p>{{ pesan }}</p>
    <input v-model = "pesan">
  </div>

    
    <table border="1">
      <tr>
      <th>No</th>
      <th>Nama</th>
      <th>Kelas</th>
      <th>Jurusan</th>
      </tr>
      <tr v-for="siswa in data">
        <td>{{ number++ }}</td>
        <td>{{ siswa.nama }}</td>
        <td>{{ siswa.kelas }}</td>
        <td>{{ siswa.jurusan }}</td>
      </tr>
    </table>
    

  
</template>