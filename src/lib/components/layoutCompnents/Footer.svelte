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
        <div class="animate-flow flex w-full justify-center gap-4 sm:gap-6 md:gap-12 lg:gap-24">
            {#each logos as logo}
                <div class="flex items-center justify-center min-w-[60px] sm:min-w-[80px] md:min-w-[120px]">
                    <img 
                        src={logo.src} 
                        alt={logo.alt} 
                        class="h-auto w-auto max-h-[25px] sm:max-h-[35px] md:max-h-[50px] opacity-40 hover:opacity-70 transition-opacity" 
                    />
                </div>
            {/each}
        </div>
    </div>
</div>

<style>
    .logo-container {
        width: 100%;
        overflow: hidden;
        position: relative;
        margin-top: 3rem;
        padding: 1rem 0;
    }

    .logo-flow {
        display: flex;
        justify-content: center;
        width: 100%;
    }

    /* Animation only applies on large screens */
    @media (min-width: 768px) {
        .animate-flow {
            animation: flow 20s linear infinite;
        }
    }

    /* Adjust animation speed for smaller screens */
    @media (max-width: 767px) {
        .animate-flow {
            animation: flow 15s linear infinite;
        }
    }

    @keyframes flow {
        0% {
            transform: translateX(100%);
        }
        100% {
            transform: translateX(-100%);
        }
    }
</style>