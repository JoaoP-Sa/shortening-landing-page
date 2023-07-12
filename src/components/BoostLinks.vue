<template>
    <section>
        <h2>Boost your links today</h2>
        <a class="btn cyan position-relative rounded-pill fw-bold text-white px-4 py-2 mt-3">Get Started</a>
    </section>
</template>

<script lang="ts">
    import { defineComponent } from 'vue';

    export default defineComponent({
        name: 'BoostLinks'
    });
</script>

<style lang="scss" scoped>
    section {
        background-image: url('../assets/bg-boost-desktop.svg');
        background-repeat: no-repeat;
        background-size: cover;
        background-color: #3a3053;
        text-align: center;
        padding: 3.5rem 0;

        h2 {
            color: white;
            font-weight: bold;
        }
    }
</style>