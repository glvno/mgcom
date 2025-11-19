<script context="module">
	import PortfolioItem from '$lib/PortfolioItem.svelte';
	export const hydrate = false;

	let portfolioItems = [
		{
			title: 'cineplex',
			uri: 'https://github.com/glvno/cineplex',
			image: '/cineplex.gif',
			description: "The world's least worst video multiplexer, written in Rust"
		},
		{
			title: 'unleaded.management',
			uri: 'https://unleaded.management',
			image: '/unleaded.jpg',

			description: "The world's least worst video multiplexer, written in Rust"
		},
		{
			title: 'raining.social',
			uri: '/',
			image: '/raining.jpg',

			description: "The world's least worst video multiplexer, written in Rust"
		}
	];
</script>

<div>
	<ul class="flex w-full flex-col items-center justify-around gap-5">
		{#each portfolioItems as pItem}
			<PortfolioItem item={pItem} />
		{/each}
	</ul>
</div>
