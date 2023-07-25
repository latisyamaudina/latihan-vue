<template>
    <div>
        <h2>{{ pesanSelamat }}</h2>
        <button @click="greet">Sapa Bro!</button>
    </div>
</template>

<script>
export default {
  props: ['nama', 'umur'],
  data() {
    return {
      pesan: 'Hallo, ' + this.nama + '!'
    };
  },
  methods: {
    greet() {
      alert('Halo, bro!');
    }
  },
  computed: {
    pesanSelamat() {
      return 'Haii, ' + this.nama + '!';
    }
  },
  watch: {
    umur(newUmur, oldUmur) {
      console.log('Umur berubah dari', oldUmur, 'menjadi', newUmur);
    }
  }
}
</script>