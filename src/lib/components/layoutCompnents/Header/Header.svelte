<script>
    import logo from '$lib/assets/logo.png';
    import NavMenu from '$lib/components/layoutCompnents/Header/NavMenu.svelte';
    
    // Define base to fix the error
    const base = '';
    
    // Add state for mobile menu toggle
    let isMenuOpen = false;
    
    // Function to toggle menu
    function toggleMenu() {
        isMenuOpen = !isMenuOpen;
    }
</script>

<header class="animate-header z-10 mx-auto mt-24 w-[80vw] rounded-md bg-transparent">
    <div class="mx-auto w-[80vw] px-4">
        <div class="flex h-auto flex-col w-full items-center justify-between py-4 lg:h-16 lg:flex-row lg:py-0 md:gap-10">
            <div class="flex w-full flex-col md:flex-row justify-between items-center gap-10 ">
                <a href="/ADC-5" class="flex flex-col  items-center">
                    <img
                        src={logo}
                        alt="Logo"
                        class="text-focus-in mx-auto mb-4 h-auto w-40 duration-200 hover:scale-105 lg:mx-0 lg:mb-0 lg:w-50"
                        loading="lazy"
                        width="160"
                        height="auto"
                    />
                    <p class="font-bold text-red-100 uppercase drop-shadow-lg text-focus-in">Gravity Grit Glory</p>
                </a>
                <!-- Hamburger Menu Button - now showing up to lg breakpoint -->
                <button 
                    class="text-white bg-red-500 p-2 mb-5 focus:outline-none lg:hidden"
                    aria-label={isMenuOpen ? "Close menu" : "Open menu"}
                    on:click={toggleMenu}
                >
                    {#if isMenuOpen}
                        <!-- X Icon for Close -->
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
                        </svg>
                    {:else}
                        <!-- Hamburger Icon -->
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
                        </svg>
                    {/if}
                </button>
            </div>
            
            <!-- Mobile Menu - now shows full menu only after lg breakpoint -->
            <div class={`w-full transition-all duration-300 ease-in-out lg:block ${isMenuOpen ? 'block' : 'hidden'}`}>
                <NavMenu />
            </div>
        </div>
    </div>
    <hr class="my-5 border-1 border-white opacity-50" />
</header>

<style>
    .animate-header {
        -webkit-animation: slide-in-left 1.5s cubic-bezier(0.25, 0.46, 0.45, 0.94) both;
        animation: slide-in-left 1.5s cubic-bezier(0.25, 0.46, 0.45, 0.94) both;
    }

    @-webkit-keyframes slide-in-left {
        0% {
            -webkit-transform: translateX(-900px);
            transform: translateX(-900px);
            opacity: 0;
        }
        100% {
            -webkit-transform: translateX(0);
            transform: translateX(0);
            opacity: 0.8;
        }
    }
    @keyframes slide-in-left {
        0% {
            -webkit-transform: translateX(-1000px);
            transform: translateX(-1000px);
            opacity: 0;
        }
        100% {
            -webkit-transform: translateX(0);
            transform: translateX(0);
            opacity: 0.8;
        }
    }

    .text-focus-in {
        -webkit-animation: text-focus-in 1.5s cubic-bezier(0.55, 0.085, 0.68, 0.53) both;
        animation: text-focus-in 1.5s cubic-bezier(0.55, 0.085, 0.68, 0.53) both;
    }

    /* Animation keyframes remain the same */
    /* ... */
</style>