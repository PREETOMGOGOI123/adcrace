<script>

	const adcImages = [
		{
			podium: [
				'https://res.cloudinary.com/dcmyqduai/image/upload/v1741456752/FINALR_1_fksvgn.webp'
			],
			title: 'Standings'
		}
	];
	import ImageCard from '$lib/components/shared/ImageCard.svelte';

</script>

{#each adcImages[0].podium as src}
	<ImageCard
		{src}
		
	/>
{/each}
