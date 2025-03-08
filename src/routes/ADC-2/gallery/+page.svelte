<script>
	import ImageGallery from '$lib/components/shared/ImageGallery.svelte';
	const galleryImages = [
		'https://res.cloudinary.com/dcmyqduai/image/upload/v1741457965/1_x3dqld.webp',
		'https://res.cloudinary.com/dcmyqduai/image/upload/v1741457957/6_ekkbqf.webp',
		'https://res.cloudinary.com/dcmyqduai/image/upload/v1741457955/7_akulfe.webp',
		'https://res.cloudinary.com/dcmyqduai/image/upload/v1741457954/8_jst6fd.webp',
		'https://res.cloudinary.com/dcmyqduai/image/upload/v1741457171/16_ji0xmy.webp',
		'https://res.cloudinary.com/dcmyqduai/image/upload/v1741457143/17_pwgjqa.webp',
		'https://res.cloudinary.com/dcmyqduai/image/upload/v1741457142/18_i3detc.webp',
		'https://res.cloudinary.com/dcmyqduai/image/upload/v1741457142/18_i3detc.webp',
		'https://res.cloudinary.com/dcmyqduai/image/upload/v1741457131/24_ocr55f.webp',
		'https://res.cloudinary.com/dcmyqduai/image/upload/v1741457139/20_1_mujk1q.webp',
		'https://res.cloudinary.com/dcmyqduai/image/upload/v1741442385/32.webp',
		'https://res.cloudinary.com/dcmyqduai/image/upload/v1741442309/28.webp',
		'https://res.cloudinary.com/dcmyqduai/image/upload/v1741442262/27.webp',
		'https://res.cloudinary.com/dcmyqduai/image/upload/v1741442261/30.webp',
		'https://res.cloudinary.com/dcmyqduai/image/upload/v1741442261/30.webp',
		'https://res.cloudinary.com/dcmyqduai/image/upload/v1741442201/29.webp',
		'https://res.cloudinary.com/dcmyqduai/image/upload/v1741442161/34.webp'
	];
	import { writable } from 'svelte/store';
	let currentIndex = writable(null);
</script>

<ImageGallery images={galleryImages} />
