<script>

	const adcImages = [
		{
			podium: [
				'https://res.cloudinary.com/dcmyqduai/image/upload/v1741441134/PODIUM_4_ynot7f.jpg',
				'https://res.cloudinary.com/dcmyqduai/image/upload/v1741441133/PODIUM_3_swdqch.jpg',
				'https://res.cloudinary.com/dcmyqduai/image/upload/v1741441133/PODIUM_2_wrruna.jpg',
				'https://res.cloudinary.com/dcmyqduai/image/upload/v1741441133/PODIUM_1_agxovr.jpg'
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
