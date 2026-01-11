<script context="module">
	import ReferralItem from '$lib/ReferralItem.svelte';
	export const hydrate = false;

	let referralItems = [
		{ url: '/endorsements/1.jpeg' },
		{ url: '/endorsements/2.jpeg' },
		{ url: '/endorsements/3.jpeg' },
		{ url: '/endorsements/4.jpeg' },
		{ url: '/endorsements/5.jpeg' },
		{ url: '/endorsements/6.jpeg' }
	];
</script>

<div>
	<ul class="flex w-full flex-col items-center justify-around gap-5">
		{#each referralItems as rItem}
			<ReferralItem item={rItem} />
		{/each}
	</ul>
</div>
