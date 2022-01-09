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
			<SidebarList url="" name="Home" on:state={handleSide} />
			<SidebarList url="about" name="About" on:state={handleSide} />
		</div>
		<div class="pb-10">
			<div class="text-xl font-bold">SvelteKit</div>
			<SidebarList url="sveltekit/typography" name="Typography" on:state={handleSide} />
			<SidebarList
				url="sveltekit/responsive-sidebar"
				name="Responsive sidebar"
				on:state={handleSide}
			/>
			<SidebarList url="sveltekit/dotenv" name="How to add dotenv" on:state={handleSide} />
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
