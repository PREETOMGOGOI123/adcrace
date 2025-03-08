<script>
    import { page } from '$app/stores';
    
    // Create a reactive statement to update currentPath when page changes
    $: currentPath = $page.url.pathname;
    $: console.log("Current path:", currentPath);
    
    // Function to check if a path is active (with or without trailing slash)
    function isActive(path) {
        return currentPath === path || currentPath === `${path}/`;
    }
</script>

<nav
    class="flex flex-col space-y-2 text-center text-gray-900 md:flex-row md:space-y-0 md:space-x-10 md:text-left justify-end items-center"
>
    <a
        href="/ADC-5"
        class={`rounded-sm px-2 font-bold duration-250 hover:scale-95 hover:text-slate-500 ${isActive('/ADC-5') ? 'active' : 'text-slate-300'}`}>
        ADC 5.0
    </a>
    <a
        href="/ADC-4"
        class={`rounded-sm px-2 font-bold duration-250 hover:scale-95 hover:text-slate-500 hover:underline ${isActive('/ADC-4') || isActive('/ADC-4/gallery') ? 'active' : 'text-slate-300'}`}>
        ADC 4.0
    </a>
    <a
        href="/ADC-3"
        class={`rounded-sm px-2 font-bold duration-250 hover:scale-95 hover:text-slate-500 hover:underline ${isActive('/ADC-3') || isActive('/ADC-3/gallery') ? 'active' : 'text-slate-300'}`}>
        ADC 3.0
    </a>
    <a
        href="/ADC-2"
        class={`rounded-sm px-2 font-bold duration-250 hover:scale-95 hover:text-slate-500 hover:underline ${isActive('/ADC-2') || isActive('/ADC-2/gallery') ? 'active' : 'text-slate-300'}`}>
        ADC 2.0
    </a>
    <a
        href="/ADC-1"
        class={`rounded-sm px-2 font-bold duration-250 hover:scale-95 hover:text-slate-500 hover:underline ${isActive('/ADC-1') || isActive('/ADC-1/gallery') ? 'active' : 'text-slate-300'}`}>
        ADC 1.0
    </a>
</nav>

<style>
    /* Make the active style stronger to ensure it overrides other styles */
    :global(nav a.active) {
        color: rgb(255, 169, 115) !important;
        text-decoration: underline !important;
        font-weight: 800 !important;
    }
</style>