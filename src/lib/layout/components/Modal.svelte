<script>
	// @ts-nocheck

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

	/**
	 * @param {any} retVal
	 */
	function close(retVal) {
		// @ts-ignore
		if (!visible) return;
		// @ts-ignore
		window.removeEventListener('keydown', keyPress);
		// @ts-ignore
		onTop = prevOnTop;
		// @ts-ignore
		if (onTop == null) document.body.style.overflow = '';
		// @ts-ignore
		visible = false;
		// @ts-ignore
		if (closeCallback) closeCallback(retVal);
	}
</script>

<!-- svelte-ignore a11y-click-events-have-key-events -->
<div class="modal-overlay" on:click={handleCloseModal}>
	<div class="modal-top" >
	<svg id="close" on:click={() => close()} viewBox="0 0 12 12">
		<circle cx="6" cy="6" r="6" />
		<line x1="3" y1="3" x2="9" y2="9" />
		<line x1="9" y1="3" x2="3" y2="9" />
	</svg>
	</div>
	<div class="modal-img">
		<!-- svelte-ignore a11y-img-redundant-alt -->
		<img src={imageUrl} alt="Modal Image" />
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
		display: flex;
		justify-content: center;
		align-items: center;
		align-content: center;
		z-index: 999;
	}

	.modal-img {
		background-color: #fff;
		padding: 0.2rem;
		box-shadow: 0 2px 4px rgba(11, 11, 11, 0.2);
	}

	.modal-top {
		position: relative;
	}

	#close {
		position: absolute;
		top: -8px;
		right: -12px;
		width: 45px;
		height: 35px;
		cursor: pointer;
		fill: #f44;
		transition: transform 0.3s;
	}

	#close:hover {
		transform: scale(2);
	}

	#close line {
		stroke: #fff;
		stroke-width: 2;
	}

	img {
		max-width: 100%;
		height: auto;
	}

	@media screen and (max-width: 480px) {
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

		#close {
			position: absolute;
			top: -10rem;
			bottom: -2rem;
			/* right: 22rem; */
			left: 21rem;
			width: 2.5rem;
			height: 3rem;
			cursor: pointer;
			fill: #f44;
			transition: transform 0.3s;
		}
	}
</style>
