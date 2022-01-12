<script>
	import Hamburger from './Hamburger.svelte';

	export let siteName = 'Demo';
</script>

<header class="bg-gray-200 py-3 px-10 items-center text-gray-600 border-b-2">
	<nav class="flex">
		<Hamburger />
		<svg width="100%" height="30">
			<text x="0" y="20">{siteName}</text>
		</svg>
	</nav>
</header>

<style>
	text {
		fill: currentColor;
	}
</style>
