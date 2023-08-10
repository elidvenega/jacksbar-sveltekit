<script>
	// @ts-nocheck

	export let imageUrl;

	export let closeModal;

	function handleCloseModal() {
		closeModal();
	}
</script>

<!-- svelte-ignore a11y-click-events-have-key-events -->
<div class="modal-overlay" on:click={handleCloseModal}>
	<div class="modal-img">
		<div class="modal-top">
			<svg class="close" on:click={handleCloseModal} viewBox="0 0 12 12">
				<circle cx="6" cy="6" r="6" />
				<line x1="3" y1="3" x2="9" y2="9" />
				<line x1="9" y1="3" x2="3" y2="9" />
			</svg>

			<!-- svelte-ignore a11y-img-redundant-alt -->
			<img src={imageUrl} alt="Modal Image" />
		</div>
	</div>
</div>

<style>
	.modal-overlay {
		position: fixed;
		top: 10%;
		left: 12%;
		width: 60%;
		margin: 0 5rem;
		background-color: rgba(11, 11, 11, 0.6);
		z-index: 20;
	}

	.modal-img {
		background-color: #fff;
		padding: 0.2rem;
		box-shadow: 0 2px 4px rgba(11, 11, 11, 0.2);
	}

	.modal-top {
		position: relative;
	}

	.close {
		position: absolute;
		top: -2%;
		right: -3%;
		width: 5%;
		cursor: pointer;
		fill: #f44;
		transition: transform 0.3s;
		z-index: 999;
	}

	.close:hover {
		transform: scale(2);
	}

	.close line {
		stroke: #fff;
		stroke-width: 2;
	}

	img {
		max-width: 100%;
		height: auto;
	}

	@media screen and (max-width: 760px) {
		.modal-overlay {
			position: fixed;
			top: 0;
			left: 0;
			width: 100%;
			margin: 0;
			min-height: 100%;
			background-color: rgba(11, 11, 11, 0.6);
			display: flex;
			justify-content: center;
			align-items: center;
			z-index: 999;
		}

		.close {
			position: absolute;
			top: -5%;
			right: 0;
			width: 10%;
		}

		.close:hover {
			transform: scale(2);
		}

		.close line {
			stroke: #fff;
			stroke-width: 2;
		}
	}
</style>
