<script context="module">
	export const hydrate = false;
	let contactLinks = [
		{title: "gh", uri: "https://github.com/glvno"},
		{title: "email", uri: "mailto:michael.glaviano@gmail.com"}
	]
</script>


	<div class="container">
	<ul>
	{#each contactLinks as link}
	<li>
		<a href={link.uri}>{link.title}</a>
	</li>
	{/each}
	</ul>

	</div>


	<style>
	.container {
		display: flex;
		align-content: center;
	}
	</style>
