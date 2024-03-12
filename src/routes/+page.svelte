<script>
	import Navbar from '$lib/layout/components/Navbar.svelte';
	import PrimaryContent from '$lib/layout/PrimaryContent.svelte';
	import FoodMenu from '$lib/layout/FoodMenu.svelte';
	import FoodModal from '$lib/layout/FoodModal.svelte';
	import FoodImages from '$lib/layout/FoodImages.svelte';
	import Footer from '$lib/layout/components/Footer.svelte';
	import '../style.css';
</script>

<Navbar />
<PrimaryContent />
<FoodMenu />
<FoodModal />
<FoodImages />
<Footer />
