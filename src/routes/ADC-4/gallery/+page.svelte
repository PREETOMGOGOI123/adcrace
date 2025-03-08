<script>
    import ImageGallery from "$lib/components/shared/ImageGallery.svelte";
    const galleryImages = [
            'https://res.cloudinary.com/dcmyqduai/image/upload/v1741440894/26_xb4gru.jpg',
            'https://res.cloudinary.com/dcmyqduai/image/upload/v1741440892/23_ssxdyu.jpg',
            'https://res.cloudinary.com/dcmyqduai/image/upload/v1741440891/25_x9kmpu.jpg',
            'https://res.cloudinary.com/dcmyqduai/image/upload/v1741440891/25_x9kmpu.jpg',
            'https://res.cloudinary.com/dcmyqduai/image/upload/v1741440886/27_ua5gez.jpg',
            'https://res.cloudinary.com/dcmyqduai/image/upload/v1741440879/20_rzavaa.jpg',
            'https://res.cloudinary.com/dcmyqduai/image/upload/v1741440876/17_ta6lde.jpg',
            'https://res.cloudinary.com/dcmyqduai/image/upload/v1741440876/18_caazfo.jpg',
            'https://res.cloudinary.com/dcmyqduai/image/upload/v1741440868/13_kijgci.jpg',
            'https://res.cloudinary.com/dcmyqduai/image/upload/v1741440858/10_lgmsm0.jpg',
            'https://res.cloudinary.com/dcmyqduai/image/upload/v1741440850/4_y1mhte.jpg',
            'https://res.cloudinary.com/dcmyqduai/image/upload/v1741440848/2_itnj7l.jpg',
            'https://res.cloudinary.com/dcmyqduai/image/upload/v1741440848/3_vql0b0.jpg'
    ]
    let currentIndex = $state(null)
</script>
<ImageGallery images = {galleryImages} />