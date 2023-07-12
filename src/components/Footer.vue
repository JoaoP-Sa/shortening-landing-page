<template>
    <footer class="row">
        <div class="col-xl-3">
            <h4>Shortly</h4>
        </div>
        <div class="col-xl-2">
            <ul>
                <span>Features</span>
                <li>List Shortening</li>
                <li>Branded Links</li>
                <li>Analytics</li>
            </ul>
        </div>
        <div class="col-xl-2">
            <ul>
                <span>Resources</span>
                <li>Blog</li>
                <li>Developers</li>
                <li>Support</li>
            </ul>
        </div>
        <div class="col-xl-2">
            <ul>
                <span>Company</span>
                <li>About</li>
                <li>Out Team</li>
                <li>Careers</li>
                <li>Contact</li>
            </ul>
        </div>
        <div class="col-xl-3 social-media-icons">
            <img src="../assets/icon-facebook.svg" alt="">
            <img src="../assets/icon-twitter.svg" alt="">
            <img src="../assets/icon-pinterest.svg" alt="">
            <img src="../assets/icon-instagram.svg" alt="">
        </div>
    </footer>
</template>

<script lang="ts">
    import { defineComponent } from 'vue';

    export default defineComponent({
        name: 'Footer',
    });
</script>

<style lang="scss" scoped>
    footer {
        background-color: #232027;
        padding: 3rem 0;

        [class^="col-xl-"]{
                text-align: center;
            }

        h4, span {
            color: white;
            font-weight: bold;
        }

        ul, li {
            text-align: left;
        }

        ul {
            li {
                list-style-type: none;
                color: #c1bec5;
                line-height: 2rem;

                &:first-of-type {
                    margin-top: 1rem;
                }
            }
        }

        .social-media-icons{
            display: flex;
            justify-content: space-between;
            padding: 0 0 !important;
            width: 8rem;
            margin: 0 auto;

            img {
                height: 1.2rem;
            }
        }
    }

    @media screen and (max-width: 1200px) {
            footer {
                display: flex !important;
                flex-direction: column;
                gap: 2.2rem;

                h4 {
                    font-size: 1.8rem;
                }

                .col-xl-2 {
                    ul {
                        padding: 0 0 !important;

                        span {
                            display: block;
                            padding-bottom: 0.2rem !important;
                        }
                    }
                    
                    ul, li {
                        text-align: center;
                    }

                    li {
                        line-height: 2.6rem;
                    }
                }

                .social-media-icons {
                    width: 14rem;

                    img {
                        height: 1.8rem !important;
                    }
                }
            }
        }
</style>