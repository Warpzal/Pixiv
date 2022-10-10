<script setup>
    import TheNavigation from './components/TheNavigation.vue'
    import Section_A from './components/sections/Section_A.vue'
    import Section_B from './components/sections/Section_B.vue'
    import Section_C from './components/sections/Section_C.vue'
    import Section_D from './components/sections/Section_D.vue'
    import Section_E from './components/sections/Section_E.vue'
    import Section_F from './components/sections/Section_F.vue'
    import Section_G from './components/sections/Section_G.vue'
</script>

<template>
    <TheNavigation class="z z--0" />
    <Section_A class="z z--1" />
    <Section_B class="z z--2" />
    <Section_C class="z z--3" />
    <Section_D class="z z--4" />
    <Section_E class="z z--5" />
    <Section_F class="z z--4" />
    <Section_G class="z z--4" />
</template>

<style lang="scss">
    //DEBUG
    // * {
    //     background: rgba(156, 55, 55, 0.1) !important;
    //     img,
    //     video,
    //     svg {
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

    #app {
        isolation: isolate;
        width: 100%;
        height: 100vh;
        overflow: hidden;
        overflow-y: auto;
        background: white;
        perspective: 10px;
    }

    .isolation {
        isolation: isolate;
        perspective: 10px;
        overflow: hidden;
        overflow-y: auto;
    }

    .z {
        &--0 {
            z-index: 1000;
        }
        &--1 {
            z-index: 20;
        }
        &--2 {
            z-index: 100;
        }
        &--3 {
            z-index: 100;
        }
        &--4 {
            z-index: 100;
        }
        &--5 {
            z-index: 20;
        }
        &--6 {
            z-index: 15;
        }
    }
</style>
