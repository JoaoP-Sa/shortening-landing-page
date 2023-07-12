<template>
    <section class="container rounded-3">
        <div class="row">
            <div class="col-xl-10 form-group">
                <input type="text" placeholder="Shorten a link here..." class="form-control py-3 px-3">
            </div>
            <div class="col-xl-2 form-group">
                <a class="btn cyan position-relative rounded-3 fw-bold text-white form-control py-3 px-3"
                    >Shorten It!</a
                    >
            </div>
        </div>
    </section>
</template>

<script lang="ts">
    import { defineComponent } from 'vue';

    export default defineComponent({
        name: 'ShortenComponent'
    });
</script>

<style scoped lang="scss">
    section {
        background-image: url('../assets/bg-boost-desktop.svg');
        background-color: #3a3053;
        padding: 3rem 4rem;
        position: relative;
        z-index: 100;
    }

    @media screen and (max-width: 1199px) {
        section {
            padding: 1.5rem 1.5rem;

            [class^="col-xl-"]{
                margin-top: 1.3rem;
    
                &:first-of-type{
                    margin-top: 0;
                }
            }
        }
    }
</style>