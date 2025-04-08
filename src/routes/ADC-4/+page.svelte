<script>

	const adcImages = [
		{
			podium: [
				"https://res.cloudinary.com/dcmyqduai/image/upload/v1741440896/full-sas_d1hcer.webp",
				"https://res.cloudinary.com/dcmyqduai/image/upload/v1741440898/hard-tail_ujiiea.webp",
				"https://res.cloudinary.com/dcmyqduai/image/upload/v1741440898/seniors_sft2ie.webp",
				"https://res.cloudinary.com/dcmyqduai/image/upload/v1741440897/juniors_g9eoyj.webp"
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
