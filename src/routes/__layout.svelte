<script>
	import '../app.css';
	import Navbar from '$lib/components/sidebar/Navbar.svelte';
	import Sidebar from '$lib/components/sidebar/Sidebar.svelte';
	let open = false;
</script>

<svelte:head />
<Sidebar bind:open />
<Navbar bind:sidebar={open} />
<div class="container mx-auto">
	<main class="p-8">
		<slot />
	</main>
</div>

<style>
	:global(*) {
		box-sizing: border-box;
	}
</style>
