<script lang="ts">
	import { triumph } from '../stores.js';
	export let l: string;
	export let t: string;
	export let ribbonSpecificTriumph: string;
export let handleHover: () => void;
export let handleLeave: () => void;

let showTriumph = () => {
	triumph.update(_t => ribbonSpecificTriumph)

}

	
</script>

<div on:mouseleave={handleLeave} on:mouseenter={handleHover} style="left: {l}px; top: {t}px;" on:mouseover={showTriumph}/>

<style>
	div {
		z-index: 100;
		position: absolute;
		float: left;
		width: 20px;
		height: 20px;
		/* outline: .5vh black solid; */
		border-radius: 50%;
		box-sizing: border-box;
	}
</style>
