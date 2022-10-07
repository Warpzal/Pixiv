<script setup>
    const props = defineProps({
        padding: {
            type: String,
            required: false,
        },
    })
</script>

<template>
    <button class="button" :style="{ padding: props.padding }">
        <slot></slot>
    </button>
</template>

<style lang="scss" scoped>
    .button {
        cursor: pointer;
        color: white;
        background: orange;
        border: none;
        border-radius: 8rem;
        font-weight: bold;
        transition: 0.4s all;
    }
</style>
