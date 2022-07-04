<script>
	import Nav from '$lib/Nav.svelte'
	import "../styles/global.css"
</script>

<div class="container">
	<title>michael glaviano</title>
<Nav />
	<main>
	<slot/>	
	</main>
</div>


	<style>
	@import url('https://fonts.googleapis.com/css2?family=Fira+Code:wght@300&family=Montserrat:wght@100&display=swap');

	.container {
		margin-left: 0%;
		max-width: 100vw;
	}
	</style>



