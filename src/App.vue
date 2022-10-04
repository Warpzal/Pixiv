<script setup>
    import TheNavigation from './components/TheNavigation.vue'
    import Section_A from './components/sections/Section_A.vue'
    import Section_B from './components/sections/Section_B.vue'
    import Section_C from './components/sections/Section_C.vue'
</script>

<template>
    <TheNavigation />
    <Section_A />
    <Section_B />
    <Section_C />
</template>

<style lang="scss">
    //DEBUG
    // * {
    //     background: rgba(156, 55, 55, 0.1) !important;
    //     img {
    //         width: 0% !important;
    //     }
    // }

    // GLOBAL VARIABLES
    :root {
        --color-primary: hsl(35, 98%, 54%);
        --color-secondary: hsl(240, 61%, 60%);
    }

    // GLOBAL STYLES
    *,
    *::after,
    *::before {
        box-sizing: border-box;
        margin: 0;
        font-family: sans-serif;
    }

    html {
        font-size: 62.5%;
        @media (max-width: 800px) {
            font-size: 60%;
        }
        @media (min-width: 2000px) {
            font-size: 80%;
        }
        @media (min-width: 4000px) {
            font-size: 125%;
        }
    }

    .app {
        position: relative;
        isolation: isolate;
    }

    .div {
        padding: 500px 100px;
    }
</style>
