<script>
	import '../../app.css';
	import Navbar from '$lib/components/newSideBar/Navbar.svelte';
	import Sidebar from '$lib/components/newSideBar/Sidebar.svelte';
	// let open = false;
	let siteName = 'Svelte Demo';
</script>

<svelte:head />
<Sidebar />
<Navbar {siteName} />
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
