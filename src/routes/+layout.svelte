<script>
	import '../app.css';
	import Nav from '$lib/Nav.svelte';
	import '../styles/global.css';
</script>

<div class="m-auto flex w-full max-w-[500px] flex-col items-center justify-around px-8 pt-16">
	<title>michael glaviano</title>
	<Nav></Nav>
	<main class="flex flex-col items-center justify-around pt-8">
		<slot></slot>
	</main>
</div>

<style>
	@import url('https://fonts.googleapis.com/css2?family=Fira+Code:wght@300&family=Montserrat:wght@100&display=swap');
</style>
