<script lang="ts">
	export let item;
</script>

<li class="flex w-full flex-col gap-3 pb-8">
	<div class="flex flex-col gap-2">
		<div class="fira font-bold">{item.title}</div>
		<div class="fira text-xs">{item.tech}</div>
	</div>
	<img src={item.image} />

	<div class="text-sm">{item.description}</div>
</li>

<style>
	.fira {
		font-family: 'Fira Code', sans-serif;
	}
</style>
