<template>
    <div>
        <Header text="aswp"></Header>
        <my-component nama="Ujang" umur="80"></my-component>
        <LatihanComponent name="akim" umur="12"></LatihanComponent>
        <LatihanDuaComponent></LatihanDuaComponent>
        <h2>WatchersComponent</h2>
        <WatchersComponent nama="uajang" umur="66"></WatchersComponent>
        <h2>eventComponent</h2>
        <EventsComponent nama="asd" umur="80" @greeted="onGreeted">
        <template #footer>
            <div>
                <p>Ini adalah event</p>
            </div>
        </template>
        <template #header>
            <div>
                <p>ini adalah header</p>
            </div>
        </template>
        </EventsComponent>
    </div>
</template>

<script setup>
import Header from './header.vue';
import MyComponent from './MyComponent.vue';
import LatihanComponent from './LatihanComponent.vue';
import LatihanDuaComponent from './LatihanDuaComponent.vue';
import WatchersComponent from './WatchersComponent.vue';
import EventsComponent from './EventsComponent.vue';

//event
import { ref } from 'vue';
const nama = ref('john');
const umur = ref(80);

const onGreeted = () => {
    console.log('kamu udah disapa,bro!')
}
</script>