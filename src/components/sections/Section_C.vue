<template>
    <section class="about grid">
        <div class="column">
            <video
                class="about__video"
                src="@/assets/Section_C_1.mp4"
                autoplay
                playsinline
                loop
            ></video>

            <h2 class="about__heading">Better Browsing</h2>
            <p class="about__paragraph">
                pixiv Premium is a subscription plan that helps you get the best
                experience out of pixiv. There is a yearly plan for 5500 JPY
                (Approx. 55 USD) or a monthly plan for 550 JPY (Approx. 5.50
                USD). There are over 15 convenient bonuses for fans and creators
                using pixiv Premium.
            </p>
        </div>

        <div class="column">
            <video
                class="about__video"
                src="@/assets/Section_C_2.mp4"
                autoplay
                playsinline
                loop
            ></video>

            <h2 class="about__heading">Enhanced Creation</h2>
            <p class="about__paragraph">
                pixiv Premium supports your creative activities through features
                like analytics access and replacing the images in your posts.
                You'll be able to showcase your artwork while further
                emphasizing your strengths. pixiv Premium will keep your
                creative juices flowing.
            </p>
        </div>
    </section>
</template>

<style lang="scss" scoped>
    .grid {
        @media (min-width: 1000px) {
            display: flex;
            gap: 5rem;
        }
    }

    .about {
        position: relative;

        z-index: 200000;
        --padding: 2rem;
        letter-spacing: 0.08rem;
        line-height: 3.5rem;
        font-weight: bold;

        padding: 5rem 5%;
        margin: 0 auto;
        background-color: white;
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
            background: url('@/assets/Section_A_4.png');
        }

        d * {
            padding-top: var(--padding);
        }

        *:last-child {
            padding-bottom: var(--padding);
        }

        &__heading {
            font-size: 3rem;
        }

        &__paragraph {
            font-size: 1.6rem;
            font-weight: bold;
        }

        &__video {
            width: 100%;
        }
    }
</style>
