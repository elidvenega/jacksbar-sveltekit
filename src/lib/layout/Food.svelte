<script lang="ts">
	import Email from './components/Email.svelte';
	import PhoneNumber from './components/PhoneNumber.svelte';
	const imgfood1 = '/images/food-1.jpg';
	const imgfood2 = '/images/food-2.jpg';
	const imgfood3 = '/images/food-3.jpg';
	const imgfood4 = '/images/food-4.jpg';
	const imgfood5 = '/images/food-5.jpg';
	const imgfood6 = '/images/food-6.jpg';
	const imgfood7 = '/images/food-7.jpg';
	const imgfood8 = '/images/food-8.jpg';

	const images: string[] = [
		imgfood1,
		imgfood2,
		imgfood3,
		imgfood4,
		imgfood5,
		imgfood6,
		imgfood7,
		imgfood8
	];
</script>

<!--Inside the bar picture -->
<div class="bar-picture">
	<div class="layer" />
	<h3 class="text-uppercase text-white z-10 font-extrabold mt-36 text-4xl md:text-5xl" id="booking">
		Book an area
	</h3>
	<button
		class="m-2 text-uppercase mb-6 text-white z-10 text-xl border-solid border-2 neutral-50 p-2"
		type="button">Make a booking</button
	>
	<h3 class="text-uppercase text-white z-10 font-extrabold text-4xl text-center md:text-5xl">
		Here the whole bar?
	</h3>
	<button
		class="m-2 text-uppercase text-white z-10 text-xl border-solid border-2 neutral-50 p-2"
		type="button">Private hire enquiry</button
	>
</div>

<!-- operating hours section -->

<div class="text-center p-9">
	<h1 class="text-uppercase text-xl">Make a booking</h1>
	<button class="booking-buttons bg-neutral-900 m-2 text-uppercase text-white p-2" type="button"
		><PhoneNumber href="tel:760-806-4646">Call To Book</PhoneNumber></button
	>
	<h1 class="text-uppercase m-5 text-xl">Opening times</h1>
	<p class="text-uppercase">Monday: Closed</p>
	<p class="text-uppercase">Tuesday - Saturday: 11:30am - 11pm</p>
	<p class="text-uppercase">Sunday: Closed</p>
	<h1 class="text-uppercase m-5 text-xl">Contact</h1>
	<p class="text-uppercase">96 ISABELLA ST, LONDON SE1 8DD</p>
	<p class="text-uppercase">TEL: 020 7928 0678</p>
	<button class="booking-buttons bg-neutral-900 m-2 text-uppercase text-white p-2" type="button"
		><Email href="mailto:evenegas_tech@outlook.com">Email</Email></button
	>
</div>

<!-- food grid pics -->
<div class=" hidden md:grid md:grid-cols-4" id="selection">
	{#each images as FoodImg}
		<div>
			<img class="w-full min-h-full" src={FoodImg} alt="Food Images" />
		</div>
	{/each}
</div>

<style>
	.bar-picture {
		background: #0c0404 url('/images/inside-bar.jpg') no-repeat center center/cover;
		display: flex;
		flex-direction: column;
		align-items: center;
		height: 85vh;
		max-width: 100%;
		position: relative;
	}

	@media screen and (min-width: 900px) {
		.bar-picture {
			height: 100vh;
		}
	}
</style>
