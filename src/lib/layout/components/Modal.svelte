<script>
	/**
	 * @type {any}
	 */
	export let imageUrl;
	/**
	 * @type {() => void}
	 */
	export let closeModal;

	function handleCloseModal() {
		closeModal();
	}
</script>

<!-- svelte-ignore a11y-click-events-have-key-events -->
<div class="modal-overlay" on:click={handleCloseModal}>
	<div class="modal-img">
		<!-- svelte-ignore a11y-img-redundant-alt -->
		<img src={imageUrl} alt="Modal Image" />
	</div>
</div>

<style>
	.modal-overlay {
		position: fixed;
		top: 0;
		left: 12em;
		width: 70%;
		min-height: 50%;
		background-color: rgba(0, 0, 0, 0.6);
		display: flex;
		justify-content: center;
		align-items: center;
		z-index: 999;
	}

	.modal-img {
		background-color: #fff;
		padding: 0.2rem;
		box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
	}

	img {
		max-width: 100%;
		height: auto;
	}
</style>
