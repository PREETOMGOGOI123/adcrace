<script>
	import { page } from '$app/stores';
	const currentPath = $page.url.pathname;
</script>

<nav
	class="flex flex-col space-y-2 text-center text-gray-900 md:flex-row md:space-y-0 md:space-x-10 md:text-left"
>
	<a
		href="/ADC-5"
		class="rounded-sm px-2 font-bold text-slate-300 duration-250 hover:scale-95 hover:text-slate-500 {currentPath ===
		'/ADC 5'
			? 'active'
			: ''}">ADC 5.0</a
	>
	<a
		href="/ADC-4"
		class="rounded-sm px-2 font-bold text-slate-300 duration-250 hover:scale-95 hover:text-slate-500 hover:underline {currentPath ===
			'/ADC-4' || currentPath === '/adc-2024/gallery'
			? 'active'
			: ''}">ADC 4.0</a
	>
	<a
		href="/ADC-3"
		class="rounded-sm px-2 font-bold text-slate-300 duration-250 hover:scale-95 hover:text-slate-500 hover:underline {currentPath ===
		'/ADC-3'
			? 'active'
			: ''}">ADC 3.0</a
	>
	<a
		href="/ADC-2"
		class="rounded-sm px-2 font-bold text-slate-300 duration-250 hover:scale-95 hover:text-slate-500 hover:underline {currentPath ===
		'/ADC-2'
			? 'active'
			: ''}">ADC 2.0</a
	>
</nav>

<style>
	.active {
		color: blueviolet;
		text-decoration: underline;
	}
</style>