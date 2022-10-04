<script setup></script>

<template>
    <section class="about">
        <h2 class="about__heading">About "pixiv"</h2>
        <p class="about__paragraph">
            pixiv is one of the biggest art communities in the world. Here,
            people share their illustrations, manga, and novels of various
            genres. 20,000 works are posted on pixiv every day from creators all
            over the world.
        </p>

        <h2 class="about__heading">About "pixiv Premium"</h2>
        <p class="about__paragraph">
            pixiv Premium is a subscription plan that helps you get the best
            experience out of pixiv. There is a yearly plan for 5500 JPY
            (Approx. 55 USD) or a monthly plan for 550 JPY (Approx. 5.50 USD).
            There are over 15 convenient bonuses for fans and creators using
            pixiv Premium.
        </p>
    </section>
</template>

<style lang="scss" scoped>
    .about {
        position: relative;
        isolation: isolate;

        --padding: 8rem;
        letter-spacing: 0.08rem;
        line-height: 3.5rem;
        font-weight: bold;

        margin: 0 auto;
        padding: 0 10%;

        &::before {
            content: '';
            position: absolute;
            z-index: -1;
            inset: 0;

            opacity: 0.3;
            background: url('@/assets/Section_A_2.png');
        }

        * {
            padding-top: var(--padding);
        }

        *:last-child {
            padding-bottom: var(--padding);
        }

        &__heading {
            font-size: 3rem;
            text-align: center;
        }

        &__paragraph {
            font-size: 1.6rem;
            font-weight: bold;
        }

        &__video {
            width: 100%;
        }

        @media (min-width: 800px) {
            padding: 0 20%;
            &__heading {
                font-size: 4rem;
            }

            &__paragraph {
                font-size: 1.9rem;
            }
        }
    }
</style>
