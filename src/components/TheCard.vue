<script setup>
    const props = defineProps({
        background: {
            type: String,
            default: '#fff7da',
        },
    })
</script>

<template>
    <div class="card">
        <h2 class="card__heading">
            <slot name="heading"></slot>
        </h2>
        <p class="card__paragraph">
            <slot name="paragraph"></slot>
        </p>
    </div>
</template>

<style lang="scss" scoped>
    .card {
        margin-top: 0.7rem;
        padding: 3rem 2rem;
        background: v-bind('props.background');
        outline: 0.3rem solid #ffbd92;
        outline-offset: 0.7rem;
        height: max-content;

        &__heading {
            width: fit-content;
            font-size: 3.6rem;
            border-bottom: 0.5rem solid #ffbd92;
            margin-bottom: 3rem;
        }
        &__paragraph {
            font-size: 2rem;
        }
    }
</style>
