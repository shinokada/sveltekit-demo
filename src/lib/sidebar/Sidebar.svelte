<script>
	import SidebarList from './SidebarList.svelte';
	export let open;
	function handleSide() {
		open = !open;
	}
</script>

<aside class="absolute w-auto h-full bg-gray-200 border-r-2 shadow-lg" class:open>
	<nav class="p-12 text-xl">
		<div class="pb-10">
			<div class="text-xl font-bold">SvelteKit</div>
			<SidebarList url="sidebar1" name="Sidebar 1" on:state={handleSide} />
			<SidebarList url="sidebar1/post1" name="Post 1" on:state={handleSide} />
		</div>
		<div class="pb-10">
			<div class="text-xl font-bold">SvelteKit</div>
			<SidebarList url="sidebar2" name="Sidebar 2" on:state={handleSide} />
			<SidebarList url="sidebar2/post1" name="Post 1" on:state={handleSide} />
		</div>
	</nav>
</aside>

<style>
	aside {
		left: -100%;
		transition: left 0.3s ease-in-out;
	}

	.open {
		left: 0;
	}
</style>
