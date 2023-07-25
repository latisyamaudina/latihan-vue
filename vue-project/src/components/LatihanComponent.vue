<template>
    <div v-if="age > 18">
        <p>Selamat Datang {{ name }}</p>
    </div>
    <div v-else>
        <p>Maaf kamu belum cukup umur</p>
    </div>
    <button @click="greet">Sapa</button>
</template>

<script>
export default {
    props: ['name','age'],
    methods:{
        greet(){
            alert("Hallo " + this.name);
        }
    },
}
</script>