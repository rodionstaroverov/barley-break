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
    $background: #81c784;
    $background-hover: lighten(#81c784, 10%);

    .plate {
        display: flex;
        width: 100px;
        height: 100px;
        box-sizing: border-box;
        background-color: $background;
        text-align: center;
        justify-content: center;
        align-items: center;
        color: #fffafa;
        font-size: 22px;
        font-family: Arial, "Helvetica Neue", Helvetica, sans-serif;
        box-shadow: inset 0 0 1px rgba(0, 0, 0, 1);
        user-select: none;

        &:hover {
            background-color: $background-hover;
            cursor: pointer;
        }

        &:active {
            background-color: darken($background-hover, 20%);
        }

        &__hidden {
            background-color: transparent;
            color: transparent;
            pointer-events: none;
        }
    }
</style>