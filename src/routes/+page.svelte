<script>
	import Navbar from '$lib/layout/components/Navbar.svelte';
	import MainImg from '$lib/layout/MainImg.svelte';
	import About from '$lib/layout/About.svelte';
	import Menu from '$lib/layout/Menu.svelte';
	import Food from '$lib/layout/Food.svelte';
	import Footer from '$lib/layout/components/Footer.svelte';
	import '../style.css';

	import Modal from '$lib/layout/components/Modal.svelte';
</script>

<Navbar />
<MainImg />
<About />
<Menu />
<div class="food-images">
	<Modal />
</div>
<Food />
<Footer />
