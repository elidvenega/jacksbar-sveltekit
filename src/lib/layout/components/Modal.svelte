<script>
	import { LightboxGallery, GalleryThumbnail, GalleryImage } from 'svelte-lightbox';

	let wineImg = '/images/b-1.jpg';
	let friendsImg = '/images/b-2.jpg';
	let desertsImg = '/images/b-3.jpg';
	let cheersImg = '/images/b-4.jpg';
	// let foodImg = '/images/b-5.jpg';
	// let beerImg = '/images/b-6.jpg';
</script>

<LightboxGallery>
	<!-- Layout-->
	<svelte:fragment slot="thumbnail">
		<GalleryThumbnail>
			<img src={wineImg} alt="Wine" />
			<img src={friendsImg} alt="friends-image" />
			<img src={desertsImg} alt="desert" />
			<img src={cheersImg} alt="cheers" />
		</GalleryThumbnail>
	</svelte:fragment>

	<GalleryImage>
		<img src={wineImg} alt="Simple lightbox" />
	</GalleryImage>
	<GalleryImage>
		<img src={friendsImg} alt="friends" />
	</GalleryImage>
	<GalleryImage>
		<img src={desertsImg} alt="Desert" />
	</GalleryImage>
	<GalleryImage>
		<img src={cheersImg} alt="Cheers" />
	</GalleryImage>
	<!-- <GalleryImage>
		<img src={foodImg} alt="Food" />
	</GalleryImage>
	<GalleryImage>
		<img src={beerImg} alt="Beer" />
	</GalleryImage> -->
</LightboxGallery>
