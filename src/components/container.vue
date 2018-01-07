<template>
    <div class="container">
        <plate v-for="item in sortedArray"
               v-text="item"
               @move="move"
               :class="{'plate__correct' : correctPlace }"/>
    </div>
</template>

<script>
    import Plate from './plate.vue';

    export default {
        name: 'container',

        components: { Plate },

        data() {
            return {
                array: [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, null],
                sortedArray: [],
                correctPlace: false,
            };
        },

        methods: {
            move() {
                console.log('move');
            },

            reset() {
                this.sortedArray = this.array.sort(this.compareRandom);
            },

            compareRandom() {
                return Math.random() - 0.5;
            }
        },

        created() {
            console.log(this.array);
            this.reset();
            console.log(this.sortedArray);
        },
    }
</script>

<style lang="scss">
    $background: #3F3F3F;

    .container {
        position: relative;
        display: flex;
        width: 400px;
        height: 400px;
        margin: 100px;
        flex-wrap: wrap;
        box-shadow: 0 0 25px rgba(0, 0, 0, .5);
        background-color: $background;
    }
</style>