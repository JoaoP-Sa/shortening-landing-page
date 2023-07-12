<template>
    <section>
        <div class="container advanced-statistcs">
            <div class="row text-center">
                <div class="col-xl-12">
                    <h2>Advanced Statistcs</h2>
                    <p class="text-gray mt-4">
                        Track how your links are performing across the web with our advanced statistics
                        dashboard.
                    </p>
                </div>
            </div>
        </div>

        <div class="benefits-container container d-flex justify-content-between">
            <div class="blue-line cyan"></div>

            <div class="benefit-box px-4 pb-4">
                <div class="img-circle px-4 py-4 rounded-circle">
                    <img src="../assets/icon-brand-recognition.svg" alt="ícone de gráfico">
                </div>
                <h4>Brand Recognition</h4>
                <p class="text-gray">
                    Boost your brand recognition with each click. Generic links don't mean a thing.
                    Branded links help instil confidence in your content.
                </p>
            </div>

            <div class="benefit-box px-4 pb-4" style="top: 2.8rem;">
                <div class="img-circle px-4 py-4 rounded-circle">
                    <img src="../assets/icon-detailed-records.svg" alt="ícone de velocímetro">
                </div>
                <h4>Detailed Records</h4>
                <p class="text-gray">
                    Gain insights into who in clicking your links. Knowing when and where people
                    engage with your content helps inform better decisions.
                </p>
            </div>
            
            <div class="benefit-box px-4 pb-4" style="top: 5.6rem;">
                <div class="img-circle px-4 py-4 rounded-circle">
                    <img src="../assets/icon-fully-customizable.svg" alt="ícone de pincéis">
                </div>
                <h4>Fully Customizable</h4>
                <p class="text-gray">
                    Improve brand awareness and content discoverability throught customizable links,
                    supercharging audience engagement.
                </p>
            </div>
        </div>
    </section>
</template>

<script lang="ts">
    import { defineComponent } from 'vue';

    export default defineComponent({
        name: 'Benefits'
    });
</script>

<style scoped lang="scss">
    section {
        background-color: #f0f1f6;
        padding: 14rem 0 8rem 0;
        position: relative;

        h2 {
            font-weight: bold;
            font-size: 3.5rem;
        }

        .advanced-statistcs {
            p {
                font-size: 1.6rem;
                line-height: 2.5rem;
                padding: 0 16.3rem;
            }
        }

        .benefits-container {
            position: relative;
            display: flex !important;
            padding: 0 0 5.7rem 0 !important;
            margin-top: 7rem;
            
            .blue-line {
                position: absolute;
                width: 100%;
                height: 0.5rem;
                left: 0;
                right: 0;
                top: 8.7rem;
                margin: 0 auto;
            }
            .benefit-box {
                background-color: white;
                position: relative;
                padding-top: 4.8rem;
                width: calc(33% - 5rem);

                .img-circle {
                    background-color: #3a3053;
                    display: inline-block;
                    position: absolute;
                    top: -2.5rem; 

                    img {
                        height: 2.2rem;
                    }
                }

                h4 {
                    font-weight: 700;
                }
            }
        }
    }

    @media screen and (max-width: 1199px) {
        section {
            padding: 10.2rem 0 5rem 0;

            h2 {
                font-size: 2rem !important;
            }
    
            .advanced-statistics {
                p {
                    font-size: 1.1rem !important;
                    line-height: 1.8rem !important;
                    padding: 0 !important;
                }
            }
        }
    }

    @media screen and (max-width: 991px) {
        .advanced-statistcs {
            p {
                padding: 0 1rem !important;
            }
        }

        .benefits-container {
            flex-direction: column;
            gap: 4rem;
            justify-content: center;
            align-items: center;
            padding: 0 0 !important;

            .benefit-box {
                text-align: center;
                width: 80% !important;

                .img-circle {
                    display: block !important;
                    margin: 0 auto !important;
                    left: 0 !important;
                    right: 0 !important;
                    width: 5rem;
                    height: 5rem;
                    text-align: center;
                }
            }

            .blue-line {
                width: 0.5rem !important;
                height: 99% !important;
                top: 0 !important;
            }
        }
    }
</style>