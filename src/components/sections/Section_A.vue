<script setup>
    import TheButton from '../TheButton.vue'
</script>

<template>
    <section class="section background">
        <img
            src="@/assets/Section_A_4.png"
            alt=""
            class="background__image background__image--4"
        />
        <img
            src="@/assets/Section_A_2.png"
            alt=""
            class="background__image background__image--2"
        />
        <img
            src="@/assets/Section_A_3.png"
            alt=""
            class="background__image background__image--3"
        />
        <img
            src="@/assets/Section_A_1.png"
            alt=""
            class="background__image background__image--1"
        />

        <div class="call-to-action">
            <p class="highlight highlight--1">pixiv Premium</p>
            <p class="highlight highlight--2">
                After the trial, keep Premium starting at JPY 458/month. Cancel
                anytime.
            </p>
            <p class="highlight highlight--3">1 month FREE trial</p>
        </div>
        <TheButton class="button">Start free Trial</TheButton>
    </section>
</template>

<style lang="scss" scoped>
    .section {
        position: relative;
        margin-top: -60px;
        width: 100%;
        height: 100vh;
        transform-style: preserve-3d;

        &::after {
            z-index: -1;
            content: '';
            display: block;
            position: absolute;
            bottom: 0px;
            left: 0px;
            width: 100%;
            height: 278px;
            background: linear-gradient(
                to top,
                rgba(0, 0, 0, 0.4) 35%,
                rgba(0, 0, 0, 0) 100%
            );
        }

        &::before {
            content: '';
            position: absolute;
            z-index: -1;
            inset: 0;
        }

        @media (min-width: 800px) {
            top: 0;
        }
    }

    .background {
        &__image {
            position: absolute;
            width: 100%;
            height: 100%;
            object-fit: cover;
            object-position: left top;

            &--1 {
                transform: translateZ(-1px) scale(1.1);
                object-position: bottom;
                @media (min-width: 800px) {
                    object-fit: contain;
                }
            }
            &--2 {
                transform: translateZ(-3px) scale(1.3);
            }
            &--3 {
                transform: translateZ(-10px) scale(2);
            }
            &--4 {
                transform: translateZ(-20px) scale(3);
            }
            &--5 {
                transform: translateZ(-4px) scale(1.4);
            }
        }
    }

    .call-to-action {
        position: absolute;
        top: 14rem;
        left: 1rem;
        max-width: 95vw;

        @media (min-width: 800px) {
            top: auto;
            bottom: 5rem;
            left: 3vw;
        }
    }

    .button {
        position: absolute;
        bottom: 3rem;
        left: 50%;
        transform: translate(-50%, -50%);

        padding: 1.3rem 2.7rem;
        font-size: 1.6rem;

        &:hover {
            transform: scale(1.05) translate(-50%, -50%);
        }

        @media (min-width: 800px) {
            left: auto;
            bottom: 5rem;
            right: 3vw;
        }
    }

    .highlight {
        position: relative;
        font-weight: bold;
        width: fit-content;
        background: black;
        color: white;
        padding: 0.32rem 0.42rem;

        &::after {
            content: '';
            visibility: hidden;
            background: white;
            color: black;
            position: absolute;
            inset: 0;
            animation: highlight 0.3s forwards;
            animation-delay: 0.8s;
            padding: 0.32rem 0.42rem;
        }

        &--1 {
            font-size: 5rem;
            margin-bottom: 0.1rem;
        }
        &--2 {
            font-size: 2rem;
            margin-bottom: 3rem;
        }
        &--3 {
            font-size: 7rem;
            @media (max-width: 800px) {
                display: none;
            }
        }
    }

    @keyframes highlight {
        from {
            width: 100%;
            visibility: visible;
        }
        to {
            width: 0%;
            visibility: hidden;
        }
    }
</style>
