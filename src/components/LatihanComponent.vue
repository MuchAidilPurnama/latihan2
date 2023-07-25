<template>
    <div>
        <h2 v-if="umur >= 18 ">Selamat Datang, {{ name }}</h2>
        <p v-else> Maaf,Kamu Belum Cukup umur</p>
        <button @click="greet">sapa</button>
    </div>
</template>

<script>
export default {
    props:['name', 'umur'],
    methods :{
        greet() {
            alert("Hallo " + this.name)
        }
    }
}
</script>