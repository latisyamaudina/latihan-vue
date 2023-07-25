<template>
  <div>
    <Header text="Ini adalah Header"></Header><br>
    <!-- <h2>Hallo Ini Adalah Komponen Utama</h2> -->
    <!-- <my-component nama = "Latisya" umur = "17"></my-component> -->
    <LatihanDuaComponent></LatihanDuaComponent>
  </div>
</template>

<script>
import Header from './components/header.vue';
import LatihanDuaComponent from './components/LatihanDuaComponent.vue';
// import MyComponent from './components/MyComponent.vue';
export default {

  components: {
    // MyComponent,
    Header
  }
}
</script>