<script>
	import { open } from './store';
	import SidebarList from './SidebarList.svelte';
</script>

<aside class="absolute w-auto h-full bg-gray-200 border-r-2 shadow-lg" class:open={$open}>
	<nav class="p-12 text-xl">
		<div class="pb-10">
			<SidebarList url="sidebar1" name="Sidebar 1" />
			<SidebarList url="sidebar1/post1" name="Post 1" />
		</div>
		<div class="pb-10">
			<SidebarList url="sidebar2" name="Sidebar 2" />
			<SidebarList url="sidebar2/post1" name="Post 1" />
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
