<template>
    <Header />
    <InitialSection />
    <ShortenComponent />
    <Benefits />
    <BoostLinks />
    <Footer />
</template>

<script lang="ts">
    import { defineComponent } from "vue";

    import Header from "./components/Header.vue";
    import InitialSection from "./components/InitialSection.vue";
    import ShortenComponent from "./components/ShortenComponent.vue";
    import Benefits from "./components/Benefits.vue";
    import BoostLinks from "./components/BoostLinks.vue";
    import Footer from "./components/Footer.vue";

    import "../node_modules/bootstrap/dist/css/bootstrap.min.css";
    import "../node_modules/bootstrap/dist/js/bootstrap.bundle.js";
    import "../node_modules/@fortawesome/fontawesome-free/css/all.min.css";

    export default defineComponent({
        name: "App",
        components: {
            Header,
            InitialSection,
            ShortenComponent,
            Benefits,
            BoostLinks,
            Footer,
        },
    });
</script>

<style lang="scss">
    @import url("style.css");
</style>
