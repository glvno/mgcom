<script>
	import Ribbon from '$lib/Ribbon.svelte';
	import { triumph } from '../stores.js';
	let currTriumph;
	triumph.subscribe((v) => {
		currTriumph = v;
	});
</script>

<div class="container">
	<h1>curriculum vitae</h1>
	<div class="hide-container">
		<div class="hide">{currTriumph}</div>
	</div>
	<div class="img-container">
		<img
			src="cv.jpg"
			alt="A show pony with its face completely obscured by dozens of county fair ribbons"
		/>
	<Ribbon />
	</div>
</div>

<style>
	img {
		margin-top: 2vw;
		max-height: 75vh;
		max-width: 90vw;
		border-radius: 50%;
	}
	.hide-container {
		height: 1.5vh;
	}

	.hide {
		display: none;
	}

	.hide-container:hover .hide {
		display: inline;
	}
	.img-container {
		position: relative;
	}
</style>
