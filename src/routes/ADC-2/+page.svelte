<script>

	const adcImages = [
		{
			podium: [
				'/ADC 2/images/standings/ADC20R~1.webp',
				'/ADC 2/images/standings/ADC20R~2.webp',
				'/ADC 2/images/standings/CONGRA~1.webp',
				'/ADC 2/images/standings/CONGRA~2.webp',
				'/ADC 2/images/standings/CONGRA~3.webp'
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
