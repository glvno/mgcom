<script>
	let navLinks = [
		/* {title: 'home', uri: '/'}, */
		{ title: 'contact', uri: '/contact' }
	];
</script>

<div class="container">
	<ul>
		<a class="moi" href="/">michael glaviano</a>
		{#each navLinks as link}
			<li>
				<a href={link.uri}>{link.title}</a>
			</li>
		{/each}
	</ul>
</div>

<style>
	.container {
		margin-left: 0px;
		font-family: 'Fira Code', sans-serif;
		max-width: 100vw;
	}
	ul {
		padding-left: 0px;
		display: flex;
		justify-content: space-between;
		margin-left: 0px;
	}
	li {
		margin-right: 10px;
	}
	.moi {
		margin-right: 5vw;
	}
</style>
