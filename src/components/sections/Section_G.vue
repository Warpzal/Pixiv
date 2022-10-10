<script setup>
    import TheButton from '../TheButton.vue'
    const data = [
        {
            image: 'https://source.pixiv.net/www/js/build/875d73f678237a77d4a6c5ee6c9d686a.png',
            title: 'Clip Studio Paint PRO/EX discount',
            description:
                'You can upgrade Clip Studio Paint to PRO/EX for a monthly fee at a special price.',
            url: '',
        },
        {
            image: 'https://source.pixiv.net/www/js/build/4cc5c7b9e0c94c86894eab1fa1b9969d.jpeg',
            title: '"sensei" Drawing Lectures',
            description: `Improve your drawing skills through sensei's video tutorials,
                    which include 33 different courses from amateur to professional.
                    With pixiv Premium, you can watch all the lectures unlimitedly.`,
            url: '',
        },
        {
            image: 'https://source.pixiv.net/www/js/build/8edf883735961b06ea7a4eef9c2567d2.jpeg',
            title: 'Printing Discounts 5% off + bonus gifts',
            description: `
                Get 5% OFF your order in any printing shop affiliated with pixiv.
                Depending on the shop, you can also enjoy novelty items.
                `,
            url: '',
        },
    ]
</script>

<template>
    <section class="section">
        <h2 class="section__main-header">Enjoy the gifts with pixiv Premium</h2>
        <div v-for="sponsor in data" class="grid">
            <img class="section__image" :src="sponsor.image" alt="" />
            <div class="section__content">
                <h3 class="section__title">{{ sponsor.title }}</h3>
                <p class="section__description">{{ sponsor.description }}</p>
                <TheButton class="section__button">Learn More</TheButton>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
    .grid {
        @media (min-width: 1000px) {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 2rem;
            justify-content: center;
            align-items: start;
        }
    }
    .section {
        --padding: 8rem;
        position: relative;
        line-height: 3.5rem;
        font-weight: bold;

        margin: 0 auto;
        margin-top: 10rem;
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

        &__image {
            width: 100%;
            max-width: 700px;
            border: 1px solid rgba(0, 0, 0, 0.3);
            margin-bottom: 1rem;
        }

        &__main-header {
            text-align: center;
            font-size: 4rem;
            line-height: 5.5rem;
            margin-bottom: 10rem;
        }

        &__title {
            padding-top: 2rem;
            font-size: 2.6rem;
        }

        &__description {
            padding: 2rem 0;
            font-size: 1.6rem;
        }

        &__button {
            padding: 1rem 2rem;
            margin-bottom: 2rem;
        }
    }
</style>
