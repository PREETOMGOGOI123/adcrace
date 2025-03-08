<script>
	let {src, alt="standings"} = $props()
	
</script>
<!-- svelte-ignore a11y_click_events_have_key_events -->
<!-- svelte-ignore a11y_no_static_element_interactions -->
<div class="mx-auto flex w-full max-w-lg items-center justify-center hover:scale-150 duration-200 hover:z-50" onclick={onclick(index)}>
	<div
		class="relative z-10 flex w-full cursor-pointer items-center overflow-hidden rounded-xl border border-slate-800 p-[1.5px]"
	>
		<div class="rotating-gradient absolute inset-0 h-full w-full"></div>
		<div class="relative z-20 flex w-full rounded-[0.60rem] bg-slate-700 p-1">
			<img
				src={src}
				class="rounded-lg "
				alt={alt}
			/>
		</div>
	</div>
</div>

<style>
	.rotating-gradient {
		background: conic-gradient(#d7ff55 80deg, transparent 120deg);
		animation: spin 3s linear infinite;
	}

	@keyframes spin {
		0% {
			transform: rotate(360deg);
		}
		100% {
			transform: rotate(0deg);
		}
	}
</style>
