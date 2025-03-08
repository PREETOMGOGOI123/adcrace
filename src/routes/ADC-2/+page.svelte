<script>

	const adcImages = [
		{
			podium: [
				'https://res.cloudinary.com/dcmyqduai/image/upload/v1741441505/ADC20R_2_lj5ghm.webp',
				'https://res.cloudinary.com/dcmyqduai/image/upload/v1741441499/ADC20R_1_yltpki.webp',
				'https://res.cloudinary.com/dcmyqduai/image/upload/v1741441501/CONGRA_1_wgm8aj.webp',
				'https://res.cloudinary.com/dcmyqduai/image/upload/v1741441496/CONGRA_3_recpy1.webp',
				'https://res.cloudinary.com/dcmyqduai/image/upload/v1741441509/CONGRA_2_yedc0e.webp'
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
