<template>
    <div class="features">
        <h2 class="features__heading">
            pixiv gets even more fun and convenient with pixiv Premium Make
            pixiv your own!
        </h2>
        <div class="grid">
            <div class="column">
                <div class="features__image features__image--1"></div>
            </div>
            <div class="column">
                <div class="features__image features__image--2"></div>
            </div>
            <div class="column">
                <div class="features__image features__image--3"></div>
            </div>
        </div>
        <div class="grid">
            <h2 class="features__feature">Discovering Works</h2>
            <h2 class="features__feature">Creating and Browsing</h2>
            <h2 class="features__feature">Sharing your Creations</h2>
        </div>
    </div>
</template>

<style lang="scss" scoped>
    .grid {
        position: absolute;
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        width: 100%;
        height: 100%;
    }

    .column {
        background: hsl(35, 98%, 54%);
    }

    .features {
        position: relative;
        width: 100%;
        height: 80vh;
        isolation: isolate;

        &__heading {
            position: absolute;
            width: 100%;
            height: 100%;
            display: flex;
            align-items: center;
            justify-content: center;
            z-index: 1000;
            padding: 1rem 5%;
            text-align: center;
            color: white;
            font-size: 3.2rem;
            @media (min-width: 800px) {
                font-size: 5rem;
            }
        }

        &__feature {
            position: relative;
            padding: 2rem 1rem;
            text-align: center;
            color: white;
            align-self: flex-end;
            font-size: 1.6rem;

            &::before {
                content: '';
                z-index: 1;
                display: block;
                position: absolute;
                bottom: 0px;
                left: 0px;
                width: 100%;
                height: 100%;
                background: linear-gradient(
                    to top,
                    rgba(0, 0, 0, 0.4) 35%,
                    rgba(0, 0, 0, 0) 100%
                );
            }

            @media (min-width: 800px) {
                font-size: 2.4rem;
            }
        }

        &__image {
            z-index: -1;
            width: 100%;
            height: 100%;
            mix-blend-mode: multiply;

            &--1 {
                background: url('@/assets/Section_D_1.png') right 30% center /
                    cover no-repeat;
            }
            &--2 {
                background: url('@/assets/Section_D_2.png') right 15% center /
                    cover no-repeat;
            }
            &--3 {
                background: url('@/assets/Section_D_3.png') right 25% center /
                    cover no-repeat;
            }
        }
    }
</style>
