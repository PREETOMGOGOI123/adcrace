<script>
    import ImageGallery from "$lib/components/shared/ImageGallery.svelte";
    const galleryImages = [
            '/ADC 4/images/gallery/1.JPG',
            '/ADC 4/images/gallery/4.JPG',
            '/ADC 4/images/gallery/5.JPG',
            '/ADC 4/images/gallery/6.JPG',
            '/ADC 4/images/gallery/7.JPG',
            '/ADC 4/images/gallery/8.JPG',
            '/ADC 4/images/gallery/9.JPG',
            '/ADC 4/images/gallery/10.JPG',
            '/ADC 4/images/gallery/11.JPG',
            '/ADC 4/images/gallery/12.JPG',
            '/ADC 4/images/gallery/13.JPG',
            '/ADC 4/images/gallery/14.JPG',
            '/ADC 4/images/gallery/15.JPG',
            '/ADC 4/images/gallery/16.JPG',
            '/ADC 4/images/gallery/17.JPG',
            '/ADC 4/images/gallery/18.JPG',
            '/ADC 4/images/gallery/19.JPG',
            '/ADC 4/images/gallery/20.JPG',
            '/ADC 4/images/gallery/21.JPG',
            '/ADC 4/images/gallery/22.JPG',
            '/ADC 4/images/gallery/23.JPG',
            '/ADC 4/images/gallery/24.JPG',
            '/ADC 4/images/gallery/25.JPG',
            '/ADC 4/images/gallery/26.JPG',
            '/ADC 4/images/gallery/27.JPG',
            '/ADC 4/images/gallery/28.JPG'
    ]
    let currentIndex = $state(null)
</script>
<ImageGallery images = {galleryImages} />