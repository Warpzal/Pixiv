<script setup>
    import TheCard from '../TheCard.vue'
    import MediaPlayer from '../MediaPlayer.vue'
</script>

<template>
    <section class="features">
        <h2 class="features__heading">Premium Features</h2>
        <h3 class="features__heading features__heading--2">
            Enjoy works with Pixiv Premium
        </h3>
        <div class="grid">
            <TheCard background="#fff7da">
                <template v-slot:heading> Search by popularity </template>
                <template v-slot:paragraph>
                    Search popular works by no. of bookmarks. Find
                    illustrations, manga, and novels for any tag, and also
                    discover popular drawing lectures.
                </template>
            </TheCard>
            <MediaPlayer>
                <template v-slot:heading>POPULAR</template>
            </MediaPlayer>
            <TheCard background="#fef6f6">
                <template v-slot:heading>Filter by Bookmarks </template>
                <template v-slot:paragraph>
                    Sort search results based on the number of bookmarks.
                </template>
            </TheCard>
        </div>
    </section>
</template>

<style lang="scss" scoped>
    .grid {
        * {
            margin-top: 5rem;
        }
        @media (min-width: 1000px) {
            margin-top: 5rem;
            display: grid;
            gap: 5rem;
            grid-template-columns: repeat(2, 1fr);
        }
    }

    .features {
        --padding: 8rem;
        position: relative;
        letter-spacing: 0.08rem;
        line-height: 3.5rem;

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
            opacity: 0.1;
            background: url('@/assets/Section_F_1.svg');
            background-size: 50%;
            background-repeat: repeat;
        }

        &__heading,
        &__paragraph {
            padding-top: var(--padding);
            font-weight: bold;
        }

        &__heading:last-child,
        &__paragraph:last-child {
            padding-bottom: var(--padding);
        }

        &__heading {
            font-size: 3rem;
            text-align: center;
            &--2 {
                padding-top: 3rem;
                padding-bottom: 3rem;
                font-size: 2.4rem !important;
            }
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
            // padding: 0 20%;
            &__heading {
                font-size: 4rem;
            }

            &__paragraph {
                font-size: 1.9rem;
            }
        }
    }
</style>
