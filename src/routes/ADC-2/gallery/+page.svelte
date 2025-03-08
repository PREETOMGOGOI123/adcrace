<script>
    import ImageGallery from "$lib/components/shared/ImageGallery.svelte";
    const galleryImages = [
           'https://res.cloudinary.com/dcmyqduai/image/upload/v1741442385/32.webp',
           'https://res.cloudinary.com/dcmyqduai/image/upload/v1741442309/28.webp',
           'https://res.cloudinary.com/dcmyqduai/image/upload/v1741442262/27.webp',
           'https://res.cloudinary.com/dcmyqduai/image/upload/v1741442261/30.webp',
           'https://res.cloudinary.com/dcmyqduai/image/upload/v1741442261/30.webp',
           'https://res.cloudinary.com/dcmyqduai/image/upload/v1741442201/29.webp',
           'https://res.cloudinary.com/dcmyqduai/image/upload/v1741442161/34.webp',
    ]
    let currentIndex = $state(null)
</script>
<ImageGallery images = {galleryImages} />