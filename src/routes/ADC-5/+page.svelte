<script>

	const adcImages = [
		{
			podium: [
				'https://res.cloudinary.com/dcmyqduai/image/upload/t_Croped/v1744133024/Full_suspension_top_5_ufqzif.png',
				'https://res.cloudinary.com/dcmyqduai/image/upload/t_Croped/v1744133024/Hardtail_and_masters_izfjyc.png',
				'https://res.cloudinary.com/dcmyqduai/image/upload/t_Croped/v1744133025/Junior_finals_top_5_n0uyyh.png'
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
