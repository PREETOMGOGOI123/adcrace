<script>
    import ImageGallery from "$lib/components/shared/ImageGallery.svelte";
    const galleryImages = [
           '/ADC 2/images/gallery/1.jpg',
            '/ADC 2/images/gallery/2.jpg',
            '/ADC 2/images/gallery/3.jpg',
            '/ADC 2/images/gallery/4.jpg',
            '/ADC 2/images/gallery/5.jpg',
            '/ADC 2/images/gallery/6.jpg',
            '/ADC 2/images/gallery/7.jpg',
            '/ADC 2/images/gallery/8.jpg',
            '/ADC 2/images/gallery/9.jpg',
            '/ADC 2/images/gallery/10.jpg',
            '/ADC 2/images/gallery/11.jpg',
            '/ADC 2/images/gallery/12.jpg',
            '/ADC 2/images/gallery/13.jpg',
            '/ADC 2/images/gallery/14.jpg',
            '/ADC 2/images/gallery/15.jpg',
            '/ADC 2/images/gallery/16.jpg',
            '/ADC 2/images/gallery/17.jpg',
            '/ADC 2/images/gallery/18.jpg',
            '/ADC 2/images/gallery/19.jpg',
            '/ADC 2/images/gallery/20.jpg',
            '/ADC 2/images/gallery/21.jpg',
            '/ADC 2/images/gallery/22.jpg',
            '/ADC 2/images/gallery/23.jpg',
            '/ADC 2/images/gallery/24.jpg',
            '/ADC 2/images/gallery/25.jpg',
            '/ADC 2/images/gallery/26.jpg',
            '/ADC 2/images/gallery/27.jpg',
            '/ADC 2/images/gallery/28.jpg',
            '/ADC 2/images/gallery/29.jpg',
            '/ADC 2/images/gallery/30.jpg',
            '/ADC 2/images/gallery/31.jpg',
            '/ADC 2/images/gallery/32.jpg',
            '/ADC 2/images/gallery/33.jpg',
            '/ADC 2/images/gallery/34.jpg'
    ]
    let currentIndex = $state(null)
</script>
<ImageGallery images = {galleryImages} />