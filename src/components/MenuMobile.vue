<template>
    <div class="menu-container rounded-3">
        <ul>
            <li>Features</li>
            <li>Pricing</li>
            <li>Resources</li>
        </ul>
        <hr />
        <ul>
            <li>Login</li>
            <li>
                <a class="btn cyan position-relative rounded-pill fw-bold text-white py-2"
                >Sign Up</a
                >
            </li>
        </ul>
    </div>
</template>

<script lang="ts">
    import { defineComponent } from 'vue';

    export default defineComponent({
        name: 'MenuMobile',
        props: {
            showMenuMobile: { type: Boolean }
        },
        watch: {
            showMenuMobile: (val) => toggle(val)
        }
    });

    function toggle(showMenuMobile: Boolean) {
        const menuContainer: HTMLElement = document.querySelector('.menu-container')!;
        const actualHeight = parseInt(window.getComputedStyle(menuContainer).getPropertyValue('height'));

        if (showMenuMobile && actualHeight === 0) {
            menuContainer!.style.display = 'block';
            menuContainer.style.height = 'auto';
                
            let elHeight = Number(parseInt(window.getComputedStyle(menuContainer).getPropertyValue('height')));
            menuContainer.style.height = '0';
        
            setTimeout(() => {
                menuContainer.style.height = elHeight.toString() + 'px';
            }, 0);
    
            return;
        }
        
        if (actualHeight === 367) {
            menuContainer.style.height = '0';
        
            menuContainer.addEventListener('transitionend', function transitionend() {
                menuContainer.style.display = 'none';
                menuContainer.removeEventListener('transitionend', transitionend);
            });
        }
        
    }
</script>

<style lang="scss" scoped>
    .menu-container {
        max-width: 900px;
        position: absolute;
        z-index: 100;
        width: 90%;
        left: 0;
        right: 0;
        top: 5.2rem;
        margin: 0 auto;
        height: 0;
        background-color: #3a3053;
        color: white;
        overflow: hidden;
        display: none;
        transition: height .5s ease;

        ul {
            text-align: center;
            margin: 2rem 0;
            padding-left: 0;

            li {
                list-style-type: none;
                font-weight: bold;
                margin-bottom: 1.6rem;
                
                &, a {
                    font-size: 1.2rem;
                }

                &:last-of-type {
                    margin-bottom: 0 !important;
                }

                a {
                    width: 75%;
                }
            }
        }

        hr {
            width: 75%;
            margin: 0 auto;
        }
    }
</style>