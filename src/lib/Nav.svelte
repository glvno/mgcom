<script>
	let navLinks = [
		/* {title: 'home', uri: '/'}, */
		{ title: 'portfolio', uri: '/portfolio' },
		{ title: 'contact', uri: '/contact' }
	];
</script>

<div class="container">
	<ul>
		<li><a class="moi" href="/">michael glaviano</a></li>
		{#each navLinks as link}
			<li>
				<a href={link.uri}>{link.title}</a>
			</li>
		{/each}
	</ul>
</div>

<style>
	.container {
		font-family: 'Fira Code', sans-serif;
		display: flex;
		justify-content: space-around;
		width: 100%;
	}
	ul {
		display: flex;
		justify-content: space-between;
	}
	li {
		padding: 1em;
	}
</style>
