<script>
	import { Aside, Nav, SidebarList, Navbar } from '@codewithshin/svelte-sidebar';
	let siteName = 'Svelte-sidebar Multiple-menu Default';
	let lists = [
		{ url: 'svelte-sidebar-multiple', name: 'Home' },
		{ url: 'svelte-sidebar-multiple/about', name: 'About' }
	];
	let lists2 = [
		{ url: 'svelte-sidebar-multiple', name: 'Home' },
		{ url: 'svelte-sidebar-multiple/about', name: 'About' }
	];
</script>

<Navbar {siteName} />
<Aside>
	<Nav>
		<h3>Menu 1</h3>
		{#each lists as list}
			<SidebarList url={list.url} name={list.name} />
		{/each}
	</Nav>
	<Nav>
		<h3>Menu 2</h3>
		{#each lists2 as list}
			<SidebarList url={list.url} name={list.name} />
		{/each}
	</Nav>
</Aside>

<main class="container mx-auto p-8">
	<slot />
</main>
