<template>
    <div id="app">
        <h1>{{ msg }}</h1>
        <img src="./img/logo.jpg">
        <input type="text" v-model="msg">
    </div>
</template>

<script>

    import getData from './util';

    export default {
        name: 'app',
        data () {
            return {
                msg: 'Welcome to Your Vue.js'
            }
        },
        created() {
            console.log('23333');
            this.fetchData();
        },
        methods: {
            async fetchData() {
                const data = await getData();
                this.msg = data;
            }
        }
    }
</script>

<style lang="scss">
    #app {
        font-family: "Avenir", Helvetica, Arial, sans-serif;

        h1 {
            color: green;
        }
    }
</style>

