<script lang="ts">
	import Ribbon from '$lib/Ribbon.svelte';
	import { triumph } from '../stores.js';
	let currTriumph: string;
	let hideClass="hide";
	triumph.subscribe((v) => {
		currTriumph = v;
	});

let handleHover = (): void => {
	hideClass = "show"
	return
}


let handleLeave = (): void => {
	hideClass = "hide"
	return
}
</script>

<div class="container" id="horse">
	<div class="hide-container">
		<div class={hideClass}>{currTriumph}</div>
	</div>
	<div class="img-container">
		<img
			src="cv.jpg"
			alt="A show pony with its face completely obscured by dozens of county fair ribbons"
		/>
	<Ribbon handleLeave={handleLeave} handleHover={handleHover} l="155" t="150" ribbonSpecificTriumph="MFA (fiction), Iowa Writers' Workshop (2015)"/>
	<Ribbon handleLeave={handleLeave} handleHover={handleHover} l="125" t="139" ribbonSpecificTriumph="Truman Capote Fellow (2013)"/>
	<Ribbon handleLeave={handleLeave} handleHover={handleHover} l="127" t="107" ribbonSpecificTriumph="Full stack engineer, Consumer Cellular (2022-present)"/>
	<Ribbon handleLeave={handleLeave} handleHover={handleHover} l="100" t="140" ribbonSpecificTriumph="Adjunt Professor, Fiction, University of Iowa (2015-2017)"/>
	<Ribbon handleLeave={handleLeave} handleHover={handleHover} l="143" t="185" ribbonSpecificTriumph="Teaching-Writing Fellow (2014)"/>
	<Ribbon handleLeave={handleLeave} handleHover={handleHover} l="128" t="250" ribbonSpecificTriumph="Full Stack Open, University of Helsinki (2021)"/>
	<Ribbon handleLeave={handleLeave} handleHover={handleHover} l="128" t="270" ribbonSpecificTriumph="Rust, Typescript, C#, Python, Express.js, .NET, Flask, Svelte, Vue, React, PostgresSQL, SQL Server"/>
	<Ribbon handleLeave={handleLeave} handleHover={handleHover} l="135" t="215" ribbonSpecificTriumph="Not unfunny"/>
	<Ribbon handleLeave={handleLeave} handleHover={handleHover} l="70" t="215" ribbonSpecificTriumph="Digital strategist for a multibilliondollar philanthropic org (2017-2022)"/>
	</div>
</div>

<style>
	img {
		margin-top: .5em;
		width: 300px;
		border-radius: 50%;
	}
	.hide-container {
		font-size: 10px;
		margin-left: 5%;
		margin-bottom: 5px;
		height: 1.5em;
	}

	.hide {
		display: none;
	}
	.show {
		display: block;
	}

	div:hover + .hide {
		display: inline;
	}
	.img-container {
		position: relative;
	}
</style>
