<script>
	import Modal from './Modal.svelte';

	let wineImg = '/images/b-1.jpg';
	let friendsImg = '/images/b-2.jpg';
	let desertsImg = '/images/b-3.jpg';
	let cheersImg = '/images/b-4.jpg';

	let modalImageUrl = '';
	let isModalVisible = false;

	const images = [wineImg, friendsImg, desertsImg, cheersImg];

	// @ts-ignore
	function handleImageClick(imageUrl) {
		modalImageUrl = imageUrl;
		isModalVisible = true;
	}

	function closeModal() {
		isModalVisible = false;
	}
</script>

<svelte:window on:keydown={(event) => event.key === 'Escape' && closeModal()} />

<ul class="flex">
	{#each images as imageUrl}
		<li>
			<!-- svelte-ignore a11y-click-events-have-key-events -->
			<!-- svelte-ignore a11y-img-redundant-alt -->
			<img
				class="w-full min-h-full"
				src={imageUrl}
				alt="Image"
				on:click={() => handleImageClick(imageUrl)}
			/>
		</li>
	{/each}
</ul>

{#if isModalVisible}
	<Modal imageUrl={modalImageUrl} {closeModal} />
{/if}


<style>
	@media(max-width: 760px) {
		ul {
			display: flex;
			flex-direction: column;
		}
	}
</style>