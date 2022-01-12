<script>
	import { Aside, Nav, SidebarList, Navbar } from '@codewithshin/svelte-sidebar';
	let siteName = 'Multiple menu items';
	export let lists = [
		{ url: '', name: 'Home' },
		{ url: 'about', name: 'About' }
	];
	export let lists2 = [
		{ url: 'item1', name: 'Item 1' },
		{ url: 'item2', name: 'Item 2' }
	];

	let headerClass = 'bg-red-200 py-3 px-10 items-center text-yellow-600 border-b-2';
	let hamburgerClass =
		'text-red-500 hover:text-red-700 cursor-pointer mr-4 border-none focus:outline-none';
	let asideClass = 'absolute w-auto h-full bg-purple-200 border-r-2 shadow-lg';
	let navClass = 'pt-6 px-12 text-xl';
	let navDivClass = 'pb-7';
</script>

<Navbar {siteName} {headerClass} {hamburgerClass} />
<Aside {asideClass}>
	<Nav {navClass} {navDivClass}>
		<h3>Menu 1</h3>
		{#each lists as list}
			<SidebarList url={list.url} name={list.name} />
		{/each}
	</Nav>
	<Nav {navClass}>
		<h3>Menu 2</h3>
		{#each lists2 as list}
			<SidebarList url={list.url} name={list.name} />
		{/each}
	</Nav>
</Aside>
