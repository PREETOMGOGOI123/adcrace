<script>
    import logoSpokehub from "$lib/assets/logos/spokehub racing white (1).png"
    import trailHeadLogo from "$lib/assets/logos/Trail Head Crew 2.png"
    import wt from "$lib/assets/logos/WT ICON Main.png"

    const logos = [{
        src: trailHeadLogo,
        alt: "trailhead logo"
    }, {
        src: logoSpokehub,
        alt: "spokehub logo"
    }, {
        src: wt,
        alt: "wt logo"
    },
    {
        src: trailHeadLogo,
        alt: "trailhead logo"
    }, {
        src: logoSpokehub,
        alt: "spokehub logo"
    }, {
        src: wt,
        alt: "wt logo"
    }]
</script>

<div class="w-full logo-container mb-0">
    <div class="logo-flow">
        <div class="flex gap-8 md:gap-24 animate-flow w-full justify-center">
            {#each logos as logo}
            <div>
                <img
                src={logo.src}
                alt={logo.alt}
                class="w-auto h-[30px] opacity-40 md:h-[50px]"
                />
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