<script setup></script>

<template>
    <section class="section">
        <div class="section__header">
            <h2 class="section__heading">
                <slot name="heading"></slot>
            </h2>
            <div class="section__menu">
                <div class="section__menu-line"></div>
                <div class="section__menu-line"></div>
            </div>
        </div>
        <div class="section__content">
            <img
                src="@/assets/Section_F_2.jpeg"
                alt=""
                class="section__image"
            />
        </div>
    </section>
</template>

<style lang="scss" scoped>
    .section {
        position: relative;
        display: flex;
        flex-direction: column;

        background: white;
        outline: 2px solid #ffbd91;
        width: 100%;
        height: 100%;

        &__header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            background: #ffbd91;
            padding: 0.3rem 1rem;
        }

        &__heading {
            color: white;
            letter-spacing: 0.4rem;
            font-size: 1.6rem;
        }

        &__image {
            width: 100%;
            height: auto;
        }
        &__menu {
            &-line {
                &:first-child {
                    margin-bottom: 0.5rem;
                }
                height: 0.5rem;
                width: 2rem;
                background: white;
            }
        }
    }
</style>
