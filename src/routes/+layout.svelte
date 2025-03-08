<script>
	import { page } from '$app/stores';
	import '../app.css';
	import Header from '$lib/components/layoutCompnents/Header/Header.svelte';
	import Footer from '$lib/components/layoutCompnents/Footer.svelte';
	let currentPath = $page.url.pathname;
	let { children } = $props();
</script>

<section class="home flex min-h-screen w-full flex-col">
	<!-- Background Pattern -->
	<div class="absolute top-0 bottom-0 left-0 right-0">
		<div
			class="relative h-[full] w-full overflow-auto bg-black [&>div]:bg-[linear-gradient(to_right,#4f4f4f2e_1px,transparent_1px),linear-gradient(to_bottom,#8080800a_1px,transparent_1px)] [&>div]:bg-[size:14px_24px]"
		>
			{#if currentPath !== '/'}
				<div class="flex flex-col pb-10 min-h-screen">
					<Header />
					<div class="">
						{@render children()}
					</div>
					<Footer />
				</div>
			{:else}
				<div class="h-[100vh]">
					{@render children()}
				</div>
			{/if}
		</div>
	</div>
</section>
