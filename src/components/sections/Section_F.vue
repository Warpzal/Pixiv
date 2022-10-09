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
            <TheCard background="#fff7da" class="grid__item grid__item--1">
                <template v-slot:heading> Search by popularity </template>
                <template v-slot:paragraph>
                    Search popular works by no. of bookmarks. Find
                    illustrations, manga, and novels for any tag, and also
                    discover popular drawing lectures.
                </template>
            </TheCard>

            <MediaPlayer
                image="Section_F_2.jpeg"
                class="grid__item grid__item--2"
            >
                <template v-slot:heading>POPULAR</template>
            </MediaPlayer>

            <TheCard background="#fef6f6" class="grid__item grid__item--3">
                <template v-slot:heading>Filter by Bookmarks </template>
                <template v-slot:paragraph>
                    Sort search results based on the number of bookmarks.
                </template>
            </TheCard>

            <MediaPlayer
                image="Section_F_3.jpeg"
                class="grid__item grid__item--4"
            >
                <template v-slot:heading>BOOKMARK</template>
            </MediaPlayer>

            <TheCard background="#f6f7fe" class="grid__item grid__item--5">
                <template v-slot:heading> Search novels by word count</template>
                <template v-slot:paragraph>
                    With this feature, you can search novels by specifying the
                    word count. This makes it easier to search for reads of a
                    certain length, such as short stories or full-fledged
                    novels!
                </template>
            </TheCard>

            <MediaPlayer
                image="Section_F_4.jpeg"
                class="grid__item grid__item--6"
            >
                <template v-slot:heading>Novel</template>
            </MediaPlayer>

            <TheCard background="#fff5fe" class="grid__item grid__item--7">
                <template v-slot:heading> Hide Ads </template>
                <template v-slot:paragraph>
                    Hide annoying ads and load pages even faster.
                </template>
            </TheCard>

            <MediaPlayer
                image="Section_F_5.jpeg"
                class="grid__item grid__item--8"
            >
                <template v-slot:heading>AD</template>
            </MediaPlayer>

            <TheCard background="#f6fffc" class="grid__item grid__item--9">
                <template v-slot:heading> Folder Organization </template>
                <template v-slot:paragraph>
                    New work by users you follow can be organized into folders.
                </template>
            </TheCard>

            <MediaPlayer
                image="Section_F_7.jpeg"
                class="grid__item grid__item--10"
            >
                <template v-slot:heading>FOLDER</template>
            </MediaPlayer>

            <TheCard background="#fff6da" class="grid__item grid__item--11">
                <template v-slot:heading> Browsing History </template>
                <template v-slot:paragraph>
                    Display works you viewed in the last 180 days. Never miss
                    good works.
                </template>
            </TheCard>

            <MediaPlayer
                image="Section_F_6.jpeg"
                class="grid__item grid__item--12"
            >
                <template v-slot:heading>History</template>
            </MediaPlayer>
        </div>
    </section>
</template>

<style lang="scss" scoped>
    .grid {
        &__item {
            margin-top: 5rem;
            &--1 {
                grid-area: a;
            }
            &--2 {
                grid-area: b;
            }
            &--3 {
                grid-area: c;
            }
            &--4 {
                grid-area: d;
            }
            &--5 {
                grid-area: e;
            }
            &--6 {
                grid-area: f;
            }
            &--7 {
                grid-area: g;
            }
            &--8 {
                grid-area: h;
            }
            &--9 {
                grid-area: i;
            }
            &--10 {
                grid-area: j;
            }
            &--11 {
                grid-area: k;
            }
            &--12 {
                grid-area: l;
            }
        }
        @media (min-width: 1000px) {
            margin-top: 0rem;
            display: grid;
            gap: 5rem;

            grid-template-areas:
                'a b'
                'd c'
                'e f'
                'h g'
                'i j'
                'l k';
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
