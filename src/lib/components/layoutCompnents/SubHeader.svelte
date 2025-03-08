<script>
	import { page } from "$app/stores";
    import SocialLinks from "../shared/SocialLinks.svelte";
    let currentPath = $page.url.pathname; 
    let pathSegments = currentPath.split('/').filter(Boolean);
    let lastSegment = pathSegments[pathSegments.length - 1];
    $inspect( lastSegment)
    
</script>
<div class="flex gap-8 mt-5 items-center justify-center">
    <nav class="page-header flex text-white justify-between items-center gap-10 rounded-md">
        <a href={lastSegment !== 'gallery' ? `${currentPath}gallery` : currentPath} class="tracking-widest mb-1 font-bold text-sm text-indigo-400 border-2 border-indigo-400 px-5 py-2 rounded-sm">Gallery</a>
    </nav>
    <SocialLinks />
</div>