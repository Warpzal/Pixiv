<script setup>
    import { gsap } from 'gsap'
    import { ScrollTrigger } from 'gsap/ScrollTrigger'

    import { onMounted } from 'vue'

    onMounted(() => {
        gsap.registerPlugin(ScrollTrigger)
        gsap.from('.animate', {
            scrollTrigger: {
                scroller: '#app',
                trigger: '.animation',
                toggleActions: 'restart none none none',
            },
            // scrollTrigger: '.about',
            duration: 0.5,
            opacity: 0,
            stagger: 0.2,
            x: '-100%',
        })
    })
</script>

<template>
    <section class="about animation" ref="about">
        <h2 class="about__heading animate">About "pixiv"</h2>
        <p class="about__paragraph animate">
            pixiv is one of the biggest art communities in the world. Here,
            people share their illustrations, manga, and novels of various
            genres. 20,000 works are posted on pixiv every day from creators all
            over the world.
        </p>

        <h2 class="about__heading animate">About "pixiv Premium"</h2>
        <p class="about__paragraph animate">
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
        --padding: 8rem;
        letter-spacing: 0.08rem;
        line-height: 3.5rem;
        font-weight: bold;

        margin: 0 auto;
        padding: 0 10%;

        &::before,
        &::after {
            content: '';
            position: absolute;
            z-index: -1;
            inset: 0;
        }

        &::before {
            background-color: white;
        }

        &::after {
            opacity: 0.3;
            background: url('@/assets/Section_A_2.png');
            background-size: cover;
            background-repeat: no-repeat;
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
            text-align: center;
        }

        &__video {
            width: 100%;
        }

        @media (min-width: 1000px) {
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
