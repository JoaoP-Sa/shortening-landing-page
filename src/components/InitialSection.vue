<template>
    <section class="initial-section container">
        <div class="row">
            <div class="col-xl-8">
                <h1>More than just shorter links</h1>
                <p class="text-gray">
                Build your brand's recognition and get detailed insights of how your
                links are performing.
                </p>
                <a class="btn cyan position-relative rounded-pill fw-bold text-white"
                >Get Started</a
                >
            </div>
            <div class="col-xl-4 image-container">
                <img src="../assets/illustration-working.svg" />
            </div>
        </div>
    </section>
</template>

<script lang="ts">
    import { defineComponent } from "vue";

    export default defineComponent({
        name: "InitialSection",
    });
</script>

<style scoped lang="scss">
    h1 {
        font-weight: bold;
        font-size: 5rem;
    }

    .initial-section {
        padding: 8rem 0 0.3rem 0;

        p {
            font-size: 1.4rem;
            font-weight: 500;
            line-height: 2.5rem;
            padding: 0 16rem 1rem 0;
        }

        .btn {
            font-size: 1.2rem;
            padding: 0.5rem 2.3rem;
        }

        .image-container {
            position: relative; 
            bottom: 4rem; 
            right: 1rem
            
            img {
                position: absolute;
            }
        }
    }

    @media screen and (max-width: 1199px) {
        h1 {
            font-size: 2.7rem;
        }
        .initial-section {
            padding: 1.2rem 0 6rem 0;
            text-align: center;

            p {
                font-size: 1.2rem;
                line-height: 2.2rem;
                padding: 1rem 0.5rem 0 !important;
            }

            .btn {
                font-size: 1.2rem;
                padding: 0.7rem 2.5rem;
            }

            .row {
            flex-direction: column-reverse;
            }

            .btn {
            font-size: 1.2rem;
            margin-top: 1.3rem;
            }

            .image-container {
                margin-bottom: 2rem;
                position: relative; 
                bottom: 0; 
                right: 0;
                
                img {
                    position: initial;
                }
            }

            p {
            padding: 0 0;
            }
        }
    }
</style>
