<script setup></script>

<template>
    <p class="highlight">
        <slot></slot>
    </p>
</template>

<style lang="scss" scoped>
    .highlight {
            font-weight: bold;
            width: fit-content;
            background: black;
            color: white;
            padding: 0.3rem 0.35rem;

            &--1 {
                font-size: 5rem;
                margin-bottom: 0.1rem;
            }
            &--2 {
                font-size: 2rem;
                margin-bottom: 3rem;
            }
            &--3 {
                font-size: 2.7rem;
            }
        }m
</style>
