<script lang="ts"> 
	import Modal from './components/Modal.svelte';

	const wineImg = '/images/b-1.jpg';
	const friendsImg = '/images/b-2.jpg';
	const desertsImg = '/images/b-3.jpg';
	const cheersImg = '/images/b-4.jpg';

	let modalImageUrl = '';
	let isModalVisible = false;

	const images: string[]  = [wineImg, friendsImg, desertsImg, cheersImg];


	function handleImageClick(imageUrl: string) {
		modalImageUrl = imageUrl;
		isModalVisible = true;
	}

	function closeModal() {
		isModalVisible = false;
	}
</script>

<svelte:window on:keydown={(event) => event.key === 'Escape' && closeModal()} />

<ul class="flex flex-col md:flex-row">
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
