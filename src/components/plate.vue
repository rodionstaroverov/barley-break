<template>
    <div class="plate" @click="move"></div>
</template>

<script>
    export default {
        name: "plate",

        methods: {
            move() {
                this.$emit('move');
            }
        },
    }
</script>

<style lang="scss">
    $background: #FF5644;
    $background-hover: #3F3F3F;
    $background-active: #595959;
    $color: #3F3F3F;
    $color-hover: #FF5644;

    .plate {
        /*position: absolute;*/
        display: flex;
        width: 100px;
        height: 100px;
        box-sizing: border-box;
        background-color: $background;
        text-align: center;
        justify-content: center;
        align-items: center;
        color: $color;
        font-size: 22px;
        font-family: 'Roboto', sans-serif;
        box-shadow: inset 0 0 1px rgba(0, 0, 0, 1);
        user-select: none;

        &:hover {
            background-color: $background-hover;
            color: $color-hover;
            cursor: pointer;
            box-shadow: none;
        }

        &:active {
            background-color: $background-active;
        }

        &__correct {
            background-color: yellowgreen;
        }

        &:empty { // __hidden
            background-color: transparent;
            color: transparent;
            pointer-events: none;
        }

        &__hidden {
            background-color: transparent;
            color: transparent;
            pointer-events: none;
        }
    }
</style>