<template>
    <div class="plate" :class="{'plate__hidden': !status }" @click="toggleStatus"></div>
</template>

<script>
    export default {
        name: "plate",

        props: {
            status: {
                type: Boolean,
                default: true,
            }
        },

        methods: {
            toggleStatus() {
                this.status = !this.status;
            },
        },
    }
</script>

<style lang="scss">
    $background: #FF5644;
    $background-hover: #3F3F3F;
    $background-active: #595959;
    $color: #595959;
    $color-hover: #FF5644;

    .plate {
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

        &__hidden {
            background-color: transparent;
            color: transparent;
            pointer-events: none;
        }
    }
</style>