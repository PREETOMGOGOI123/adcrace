<script>
	let { images = [] } = $props();
	let currentIndex = $state(0);
	let isImageOpen = $state(false);
	const handleClick = (index, e) => {
		e.preventDefault();
		e.stopPropagation();
		currentIndex = index;
		isImageOpen = true;
	};
	const nextImage = () => {
		currentIndex !== images.length - 1 ? (currentIndex += 1) : currentIndex;
	};
	const prevImage = () => {
		currentIndex !== 0 ? (currentIndex -= 1) : currentIndex;
	};
</script>

<div class="flex flex-col items-center justify-center gap-5 duration-750">
	<div class="md:flex items-center gap-8">
		<!-- svelte-ignore a11y_consider_explicit_label -->
		<button
			class="flex h-fit w-fit cursor-pointer items-center justify-center rounded-sm bg-blue-600 p-2"
			onclick={prevImage}
			><i class="fa-solid fa-backward text-2xl" style="color: #ffffff;"></i></button
		>
		<div class="image-container">
			<!-- svelte-ignore a11y_img_redundant_alt -->
			<img
				id="mainImage"
				class="h-auto w-80 rounded-lg object-cover object-center transition-opacity duration-500 md:h-[480px] md:w-[30rem] lg:w-[50rem]"
				src={images[currentIndex]}
				alt="focused image"
			/>
		</div>
		<!-- svelte-ignore a11y_consider_explicit_label -->
		<button
			class="flex h-fit w-fit cursor-pointer items-center justify-center rounded-sm bg-blue-600 p-2"
			onclick={nextImage}
			><i class="fa-solid fa-forward text-2xl" style="color: #ffffff;"></i></button
		>
	</div>
	<div class="custom-scrollbar flex w-[80vw] px-12 gap-8 overflow-x-auto pb-4">
		{#each images as image, index}
			<div
				class="z-50 h-24 min-w-[9rem] bg-black {currentIndex === index ? 'ring-2 ring-white' : ''}"
			>
				<!-- svelte-ignore a11y_click_events_have_key_events -->
				<!-- svelte-ignore a11y_no_noninteractive_element_interactions -->
				<img
					src={image}
					class="h-24 w-36 cursor-pointer rounded-lg object-cover object-center {currentIndex ===
					index
						? 'opacity-100'
						: 'opacity-70 hover:opacity-90'}"
					alt="images"
					onclick={(e) => {
						handleClick(index, e);
					}}
				/>
			</div>
		{/each}
	</div>
</div>

<style>
	/* Custom scrollbar styling */
	.custom-scrollbar::-webkit-scrollbar {
		height: 10px;
	}

	.custom-scrollbar::-webkit-scrollbar-track {
		background: rgba(0, 0, 0, 0.2);
		border-radius: 10px;
        opacity: 0.6;
	}

	.custom-scrollbar::-webkit-scrollbar-thumb {
		background: rgba(255, 255, 255, 0.3);
		border-radius: 10px;
	}

	.custom-scrollbar::-webkit-scrollbar-thumb:hover {
		background: rgba(255, 255, 255, 0.5);
	}

	/* Firefox scrollbar styling */
	.custom-scrollbar {
		scrollbar-width: thin;
		scrollbar-color: rgba(255, 255, 255, 0.3) rgba(0, 0, 0, 0.2);
	}

	/* Image transition styles */
	.image-container {
		position: relative;
		overflow: hidden;
	}

	#mainImage {
		transition: all 0.5s ease;
	}

	/* Rest of your styles */
</style>
