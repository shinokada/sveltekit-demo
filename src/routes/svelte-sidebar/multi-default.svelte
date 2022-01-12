<script>
	import { Aside } from '@codewithshin/svelte-sidebar';
	import { Nav } from '@codewithshin/svelte-sidebar';
	import { SidebarList } from '@codewithshin/svelte-sidebar';
	import { Navbar } from '@codewithshin/svelte-sidebar';
	let siteName = 'Svelte-sidebar Multiple-menu Default';
	let lists = [
		{ url: 'svelte-sidebar', name: 'Svelte-sidebar Home' },
		{ url: 'svelte-sidebar/default', name: 'Sidebar Default' },
		{ url: 'svelte-sidebar/custom', name: 'Sidebar Custom Style' },
		{ url: 'svelte-sidebar/multi-default', name: 'Multi-menu Default' },
		{ url: 'svelte-sidebar/multi-custom', name: 'Multip-menu Custom Style' }
	];
	let lists2 = [
		{ url: 'svelte-sidebar', name: 'Svelte-sidebar Home' },
		{ url: 'svelte-sidebar/default', name: 'Sidebar Default' },
		{ url: 'svelte-sidebar/custom', name: 'Sidebar Custom Style' },
		{ url: 'svelte-sidebar/multi-default', name: 'Multi-menu Default' },
		{ url: 'svelte-sidebar/multi-custom', name: 'Multip-menu Custom Style' }
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
	<h1>{siteName}</h1>
</main>
