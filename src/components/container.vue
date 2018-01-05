<template>
    <div class="container">
        <plate v-text="1"></plate>
        <plate v-text="2"></plate>
        <plate v-text="3"></plate>
        <plate v-text="4"></plate>
        <plate v-text="5"></plate>
        <plate v-text="6"></plate>
        <plate v-text="7"></plate>
        <plate v-text="8"></plate>
        <plate v-text="9"></plate>
        <plate v-text="10"></plate>
        <plate v-text="11"></plate>
        <plate v-text="12"></plate>
        <plate v-text="13"></plate>
        <plate v-text="14"></plate>
        <plate v-text="15"></plate>
        <plate v-text="null" :status="false"></plate>
    </div>
</template>

<script>
    import Plate from './plate.vue';

    export default {
        name: 'container',

        components: { Plate },
    }
</script>

<style>
    .container {
        display: flex;
        width: 400px;
        height: 400px;
        flex-wrap: wrap;
        box-shadow: 0px 0px 5px rgba(0, 0, 0, .8);
        background-image: url('../assets/img/container.jpg');
        background-size: 100%;
    }
</style>