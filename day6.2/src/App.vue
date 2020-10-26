<template>
    <div id="app">
        {{ $store.state.num }}
        <img src="./assets/logo.png">
        <button @click="add">按钮</button>
        <router-view/>
    </div>
</template>

<script>
export default {
    name: 'App',
    methods: {
        add() {
            this.$store.commit('add_num')
        }
    }
}
</script>

<style>
#app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
}
</style>
