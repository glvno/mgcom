<script lang="ts">
	export let item;
</script>

<li class="flex w-full flex-col gap-3 pb-8">
	<div class="fira font-bold">{item.title}</div>
	<img src={item.image} />

	<div class="text-sm">{item.description}</div>
</li>

<style>
	.fira {
		font-family: 'Fira Code', sans-serif;
	}
</style>
