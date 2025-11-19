<script context="module">
	import PortfolioItem from '$lib/PortfolioItem.svelte';
	export const hydrate = false;

	let portfolioItems = [
		{ title: 'cineplex', uri: 'https://github.com/glvno/cineplex', image: '/cineplex.gif' },
		{ title: 'unleaded.management', uri: 'https://unleaded.management', image: '/unleaded.jpg' },
		{ title: 'raining.social', uri: '/', image: '/raining.jpg' }
	];
</script>

<div>
	<ul class="flex w-full flex-col items-center justify-around gap-5">
		{#each portfolioItems as pItem}
			<PortfolioItem item={pItem} />
		{/each}
	</ul>
</div>
