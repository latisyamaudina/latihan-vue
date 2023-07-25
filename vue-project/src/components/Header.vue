<template>
    <div>
        <Header text="Ini Adalah Header">
            <template #footer>
                <p>Ini Adalah Slot Dari Footer</p>
            </template>
        </Header>
        <!-- <h3>{{ text }}</h3> -->
        <my-component nama = "Latisya" umur = "17"></my-component>
        <LatihanComponent name="Latisya" age="20"></LatihanComponent>
        <LatihanDuaComponent></LatihanDuaComponent>
        <h2>WatchersComponent</h2>
        <WatchersComponent nama="Latisya" umur="8"></WatchersComponent>
        <h2>Event Component</h2>
        <EventsComponent :nama="nama" :umur="umur" @greeted="onGreeted">
        <template #footer>
            <div>
                 <p>Ini Adalah Footer Latihan Event</p>
            </div>
            </template>
            <template #header>
            <div>
                <p>Ini Adalah Header latihan Event</p>
            </div>
            </template>
        </EventsComponent>
    </div>
</template>

<script setup>
// export default {
//     name: 'Header',
//     props: ['text']
// }
import EventsComponent from './EventsComponent.vue'
import MyComponent from './MyComponent.vue';
import LatihanComponent from './LatihanComponent.vue';
import WatchersComponent from './WatchersComponent.vue';
import LatihanDuaComponent from './LatihanDuaComponent.vue';

//event
import {ref} from 'vue';
const nama = ref('Latisya');
const umur = ref(17);

const onGreeted = () => {
    console.log('Kamu sudah di sapa!')
};
</script>

<style>
/* h3 {
    color: black;
    background-color: cadetblue;
    text-align: center;
} */
</style>