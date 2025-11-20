<script context="module">
	import PortfolioItem from '$lib/PortfolioItem.svelte';
	export const hydrate = false;

	let portfolioItems = [
		{
			title: 'cineplex',
			uri: 'https://github.com/glvno/cineplex',
			image: '/cineplex.gif',
			description: "The world's least worst video multiplexer, written in Rust.",
			tech: 'Rust, iced'
		},
		{
			title: 'unleaded.management',
			uri: 'https://unleaded.management',
			image: '/unleaded.jpg',
			description: 'Replace every non-engineer at your company, yourself included, with LLMs.',
			tech: 'SvelteKit, Postgres, RAG w/ pgvector'
		},
		{
			title: 'raining.social',
			uri: '/',
			image: '/raining.jpg',
			description: "Weather-gated social media. If it ain't rainin, you ain't scrollin.",
			tech: 'Elixir, Phoenix, Svelte, Postgres'
		},

		{
			title: 'programming rust, 3rd edition (technical reviewer)',
			uri: '/',
			image: '/3e.jpg',
			description: "Not sure why they let anywhere near this, but I'm glad they did.",
			tech: 'pdf sticky notes lol'
		},
		{
			title: 'randy: game-theory-optimal poker made less impossible',
			uri: '/',
			image: '/randy.jpg',
			description:
				"He'll give you anything you want, so long as you want a random integer from 0 to 99.",
			tech: 'Rust, Tauri'
		},
		{
			title: 'rocketballs',
			uri: '/',
			image: '/ballgame.gif',
			description: 'More slide = more higher',
			tech: 'C#, Unity, prototyped in Rust w/ Bevy'
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
