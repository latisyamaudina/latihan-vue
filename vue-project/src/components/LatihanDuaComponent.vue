<template>
    <div>
        <input type="text" v-model="cari" placeholder="Cari Data">
        <ul>
            <li v-for="item in cariData" key="item.id">
                {{item.title}} - {{item.price}}
            </li>
        </ul>
    </div>
    <div v-if="cari < products" > 
    </div>
    <div v-else>
        <p>Hasil tidak di temukan</p>
    </div>
</template>

<script>
export default {
    data() {
        return {
            cari:'',
            products: []

        };
    },
    created() {
        this.products = [
            {id: 1,title:"Baju Anak",price:25000},
            {id: 2,title:"Susu Anak",price:75000},
            {id: 3,title:"Topi",price:10000},
            {id: 4,title:"Balon",price:1000},
            {id: 5,title:"KinderJoy",price:15000}
        ]
    },
    computed: {
        cariData() {
            return this.products.filter((item) => {
                return item.title.match(this.cari);
            });
        }
    }
}
</script>