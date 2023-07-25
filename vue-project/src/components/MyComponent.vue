<template>
    <div>
        <h1>Hallo Dunia</h1>
        <p>Ini Komponen Saya</p>
        <!--props-->
        <h2>Nama Saya: {{ nama }}</h2>
        <p>Umur Saya: {{ umur }}</p>
    </div>
</template>

<script>
export default {
    name: "MyComponent",
    props: ['nama','umur'],
    data() {
        return{
            message: "Ini Pesan Dari Komponen"
        }
    },
    methods: {
        greet() {
            console.log("Hallo");
        }
    },
}
</script>

<style>
h1 {
    color:rgb(110, 110, 170);
}

p{
    size: 16px;
}
</style>