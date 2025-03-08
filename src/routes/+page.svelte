<script>
	import { onMount } from 'svelte';
	import logo from '$lib/assets/logo.png';
	import Loader from '$lib/components/ui/Loader.svelte';
	onMount(() => {
		setTimeout(() => {
			window.location.href = '/ADC-5';
		}, 5600);
	});
</script>

<section class="rotate-out-left flex h-full w-full flex-col items-center justify-center">
	<div>
		<div class="flex flex-col items-center mb-5">
			<img src={logo} alt="Adc Logo" class="mx-auto" />
			<p class="md:text-6xl text-2xl font-bold text-white uppercase tracking-widest">Gravity Grit Glory</p>
		</div>
		<div class="flex justify-between">
			<Loader />
			<Loader />
			<Loader />
			<Loader />
			<Loader />
			<Loader />
		</div>
	</div>
</section>

<style>
	.rotate-out-left {
		-webkit-animation: swirl-out-bck 0.6s 4.6s ease-in both;
		animation: swirl-out-bck 0.6s 5.6s ease-in both;
	}

	@-webkit-keyframes swirl-out-bck {
		0% {
			-webkit-transform: rotate(0) scale(1);
			transform: rotate(0) scale(1);
			opacity: 1;
		}
		100% {
			-webkit-transform: rotate(-540deg) scale(0);
			transform: rotate(-540deg) scale(0);
			opacity: 0;
		}
	}
	@keyframes swirl-out-bck {
		0% {
			-webkit-transform: rotate(0) scale(1);
			transform: rotate(0) scale(1);
			opacity: 1;
		}
		100% {
			-webkit-transform: rotate(-540deg) scale(0);
			transform: rotate(-540deg) scale(0);
			opacity: 0;
		}
	}
</style>
