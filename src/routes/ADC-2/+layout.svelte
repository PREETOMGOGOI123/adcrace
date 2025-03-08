<script>
    import SubHeader from "$lib/components/layoutCompnents/SubHeader.svelte";
    let {children} =$props()
</script>
<div class="flex flex-col gap-10 items-center mb-24">
    <div class="flex">
        <SubHeader />
    </div>
    <div class="flex md:flex-row justify-center flex-col md:px-24 px-5">
        {@render children()}
    </div>
</div>