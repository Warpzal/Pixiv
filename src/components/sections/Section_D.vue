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
            <div class="features__feature">
                <h2>Discovering Works</h2>
                <svg viewBox="0 0 59 12">
                    <path
                        d="M29.6022 7.9494L57.9905 0.54834L58.7473 3.45131L29.6 11.0502L0.619583 3.45076L1.38054 0.548877L29.6022 7.9494Z"
                    ></path>
                </svg>
            </div>
            <div class="features__feature">
                <h2>Creating and Browsing</h2>
                <svg viewBox="0 0 59 12">
                    <path
                        d="M29.6022 7.9494L57.9905 0.54834L58.7473 3.45131L29.6 11.0502L0.619583 3.45076L1.38054 0.548877L29.6022 7.9494Z"
                    ></path>
                </svg>
            </div>
            <div class="features__feature">
                <h2>Sharing your Creations</h2>
                <svg viewBox="0 0 59 12">
                    <path
                        d="M29.6022 7.9494L57.9905 0.54834L58.7473 3.45131L29.6 11.0502L0.619583 3.45076L1.38054 0.548877L29.6022 7.9494Z"
                    ></path>
                </svg>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
    .grid {
        position: absolute;
        display: grid;
        grid-template-rows: repeat(3, 1fr);
        width: 100%;
        height: 100%;

        @media (min-width: 800px) {
            grid-template-columns: repeat(3, 1fr);
            grid-template-rows: auto;
        }

        svg {
            animation: bounce 2s infinite;
        }
    }

    @keyframes bounce {
        0% {
            transform: translateY(0);
        }
        50% {
            transform: translateY(10px);
        }
        100% {
            transform: translateY(0);
        }
    }

    .column {
        background: hsl(35, 98%, 54%);
    }

    .features {
        cursor: pointer;
        position: relative;
        width: 100%;
        height: 70vh;
        isolation: isolate;
        overflow: hidden;
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

        &__heading {
            display: none;
            @media (min-width: 800px) {
                display: flex;
                font-size: 5rem;
                position: absolute;
                width: 100%;
                height: 100%;
                align-items: center;
                justify-content: center;
                padding: 1rem 15%;
                text-align: center;
                color: white;
                z-index: 1;
            }
        }

        &__feature {
            display: flex;
            flex-direction: column;
            align-items: center;

            position: relative;
            padding: 2rem 1rem;
            align-self: flex-end;
            font-size: 1.6rem;

            isolation: isolate;
            h2 {
                text-align: center;
                color: white;
            }

            &::before {
                content: '';
                z-index: -1;
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

            svg {
                margin-top: 1rem;
                display: block;
                padding: 1rem;
                width: 8rem;
                color: white;
                fill: white;
            }

            @media (min-width: 800px) {
                h2 {
                    font-size: 2.4rem;
                }
            }
        }

        &__image {
            width: 100%;
            height: 100%;
            mix-blend-mode: multiply;
            filter: blur(2px);
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
