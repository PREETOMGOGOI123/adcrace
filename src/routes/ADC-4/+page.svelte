<script>

	const adcImages = [
		{
			podium: [
				'/ADC 4/images/standings/seniors.webp',
				'/ADC 4/images/standings/juniors.webp',
				'/ADC 4/images/standings/hard-tail.webp',
				'/ADC 4/images/standings/full-sas.webp'
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
