<script>
	import logoSpokehub from '$lib/assets/logos/spokehub racing white (1).png';
	import trailHeadLogo from '$lib/assets/logos/Trail Head Crew 2.png';
	import wt from '$lib/assets/logos/WT ICON Main.png';
	import pfac from '$lib/assets/logos/PFAC Logo.png';

	const logos = [
		{
			src: logoSpokehub,
			alt: 'spokehub logo'
		},
		{
			src: trailHeadLogo,
			alt: 'trailhead logo'
		},
		{
			src: wt,
			alt: 'wt logo'
		},
		{
			src: pfac,
			alt: 'pfac logo'
		},
		{
			src: trailHeadLogo,
			alt: 'trailhead logo'
		},
		{
			src: wt,
			alt: 'wt logo'
		},
		{ src: pfac, alt: 'pfac logo' },
		{
			src: logoSpokehub,
			alt: 'spokehub logo'
		}
	];
</script>

<div class="logo-container mb-0 w-full">
	<div class="logo-flow">
		<div class="animate-flow flex w-full justify-center gap-8 md:gap-24">
			{#each logos as logo}
				<div>
					<img src={logo.src} alt={logo.alt} class="h-[30px] w-auto opacity-40 md:h-[50px]" />
				</div>
			{/each}
		</div>
	</div>
</div>

<style>
	.logo-container {
		width: 100vw;
		overflow: hidden;
		position: relative;
		margin-top: 5rem;
	}

	.logo-flow {
		display: flex;
		justify-content: center;
	}

	/* Animation only applies on large screens */
	.animate-flow {
		animation: flow 20s linear infinite;
	}

	@keyframes flow {
		0% {
			transform: translateX(100%);
		}
		100% {
			transform: translateX(-100%);
		}
	}

	/* Media query for small screens */
	@media (max-width: 768px) {
		.logo-flow {
			justify-content: center;
			width: 100%;
		}
	}
</style>
