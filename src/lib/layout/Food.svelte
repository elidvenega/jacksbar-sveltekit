<script>
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
</script>

<!--Inside the bar picture -->
<div class="bar-picture">
	<div class="layer" />
	<h3 class="text-uppercase text-white z-10 font-extrabold mt-36 text-5xl" id="booking">
		Book an area
	</h3>
	<button
		class="m-2 text-uppercase mb-6 text-white z-10 text-xl border-solid border-2 neutral-50 p-2"
		type="button">Make a booking</button
	>
	<h3 class="text-uppercase text-white z-10 font-extrabold text-5xl">Here the whole bar?</h3>
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
<div class="grid grid-cols-4 overflow-hidden" id="selection">
	<div>
		<img class="h-full max-w-full object-cover" src={imgfood1} alt="food-img-1" />
	</div>
	<div>
		<img class="h-full max-w-full object-cover" src={imgfood2} alt="food-img-2" />
	</div>
	<div>
		<img class="h-full max-w-full object-cover" src={imgfood3} alt="food-img-3" />
	</div>
	<div>
		<img class="h-full max-w-full object-cover" src={imgfood4} alt="food-img-4" />
	</div>
	<div>
		<img class="h-full max-w-full object-cover" src={imgfood5} alt="food-img-5" />
	</div>
	<div>
		<img class="h-full max-w-full object-cover" src={imgfood6} alt="food-img-6" />
	</div>
	<div>
		<img class="h-full max-w-full object-cover" src={imgfood7} alt="food-img-7" />
	</div>
	<div>
		<img class="h-full max-w-full object-cover" src={imgfood8} alt="food-img-8" />
	</div>
</div>

<style>
	.bar-picture {
		background: #0c0404 url('/images/inside-bar.jpg') no-repeat center center/cover;
		display: flex;
		flex-direction: column;
		align-items: center;
		height: 100vh;
		max-width: 100%;
		position: relative;
	}
</style>
