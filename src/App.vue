<script setup>
    import TheNavigation from './components/TheNavigation.vue'
    import Section_A from './components/sections/Section_A.vue'
    import Section_B from './components/sections/Section_B.vue'
    import Section_C from './components/sections/Section_C.vue'
    import Section_D from './components/sections/Section_D.vue'
    import Section_E from './components/sections/Section_E.vue'
</script>

<template>
    <TheNavigation />
    <Section_A />
    <Section_B />
    <Section_C />
    <Section_D />
    <section class="parallax__section">
        <Section_E />
        <div class="lorem">
            Lorem, ipsum dolor sit amet consectetur adipisicing elit. Numquam
            corporis cupiditate, pariatur aliquam sed quasi dignissimos
            architecto maxime praesentium culpa porro beatae voluptatum minima
            id, accusantium enim veniam sint. Vero necessitatibus maiores
            quaerat, nemo voluptatibus aut enim ipsa exercitationem praesentium
            culpa ipsam ex ratione velit laudantium ducimus ullam nobis omnis
            repudiandae deserunt sapiente sunt deleniti accusamus. Aspernatur
            veritatis omnis exercitationem ipsum ut quia accusamus. Possimus a,
            perferendis, cum optio similique delectus ipsa deserunt dicta
            tenetur temporibus assumenda quasi nulla laudantium modi neque
            excepturi voluptas quaerat quam? Est quis porro aliquid
            exercitationem error fugit quasi incidunt autem laborum, veniam ea
            atque fuga esse doloremque culpa eveniet necessitatibus reiciendis
            itaque reprehenderit. Ad laudantium facere dolorum, quibusdam
            explicabo fuga fugit odio perferendis nihil aperiam deleniti odit
            omnis provident accusantium. Nostrum atque quas vero enim libero,
            nemo architecto impedit, inventore ipsam repudiandae at ducimus!
            Delectus ab quos, in porro atque ea? Voluptatem expedita, cum
            dolores eaque et consequuntur nemo a mollitia numquam dolor cumque
            sint eius, illo impedit vero obcaecati maxime temporibus sunt id
            sed? Similique, consequuntur. Suscipit dolorum delectus tempore
            accusantium ipsam eos, eveniet, incidunt repellendus sit eaque,
            consequatur perferendis explicabo temporibus natus. Numquam enim
            incidunt vitae iste exercitationem. Qui voluptas ex nemo?
        </div>
    </section>
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

    .app {
        // position: relative;
        // isolation: isolate;
    }

    .div {
        padding: 500px 100px;
    }

    .parallax__section {
        width: 100%;
        height: 80vh;
        overflow: hidden;
        overflow-y: auto;
        background: #ffffdb;
        perspective: 10px;
    }
    .lorem {
        background: gray;
        padding: 5rem;
        font-size: 2rem;
        color: white;
    }
</style>
