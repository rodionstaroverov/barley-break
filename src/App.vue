<template>
    <div id="app">
       <container></container>
    </div>
</template>

<script>
    import Container from './components/container.vue'

    export default {
        name: 'app',

        components: { Container },

        data() {
            return {
                msg: 'Welcome to Your Vue.js App'
            }
        }
    }
</script>

<style>
    html, body {
        margin: 0;
        padding: 0;
        width: 100%;
        height: 100%;
    }

    #app {
        display: flex;
        flex: 1;
        height: 100%;
        justify-content: center;
        align-items: center;
        background-image: url('assets/img/app.jpg');
        background-position: center bottom;
        background-attachment: fixed;
        background-size: 100%;
    }
</style>
