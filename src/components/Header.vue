<template>
	<header class="p-4">
		<div class="container">
			<div class="row d-flex">
				<nav class="col-md-6 justify-content-start d-flex desktop-screen">
					<img src="../assets/logo.svg" alt="logo" class="mr-4" />
					<ul class="nav ml-4">
						<li><a href="#" class="nav-link text-gray">Features</a></li>
						<li><a href="#" class="nav-link text-gray">Pricing</a></li>
						<li><a href="#" class="nav-link text-gray">Resources</a></li>
					</ul>
				</nav>

				<nav class="col-md-12 d-flex justify-content-between mobile-screen">
					<img src="../assets/logo.svg" alt="logo" class="mr-4" />
					<i class="fas fa-bars text-gray" style="font-size: 1.7rem;" @click="toggle()"></i>
				</nav>

				<div class="text-end col-md-6 p-0 desktop-screen">
					<a class="text-gray mx-4">Login</a>
					<a
						class="btn cyan ml-4 position-relative rounded-pill px-4 py-2 fw-bold text-white"
						style="bottom: 0.1rem"
						>Sign Up</a
					>
				</div>
			</div>
		</div>

		<MenuMobile :showMenuMobile="showMenuMobile" />
	</header>
</template>

<script lang="ts">
	import { defineComponent } from "vue";
	import MenuMobile from "./MenuMobile.vue";

	export default defineComponent({
    name: "Header",
    components: { 
		MenuMobile 
	},
	data () {
		return {
			showMenuMobile: false,
		}
	},
	methods: {
            toggle() {
				this.showMenuMobile = !this.showMenuMobile;
			},
        }
	});
</script>

<style scoped lang="scss">
	header {
		position: relative;

		a {
			font-weight: 600;
		}
	}
</style>
