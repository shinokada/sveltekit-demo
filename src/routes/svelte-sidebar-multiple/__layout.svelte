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

	let headerClass = 'bg-blue-500 py-3 px-10 items-center text-white border-b-2';
	let hamburgerClass =
		'text-blue-900 hover:text-indigo-100 cursor-pointer mr-4 border-none focus:outline-none';
	let asideClass = 'absolute w-auto h-full bg-blue-500 border-r-2 shadow-lg';
	let navClass = 'pt-6 px-12';
	let navDivClass = 'pb-7 text-white';
	let sideBarListClass = 'text-white border-gray-100 mb-2 px-4 hover:text-gray-300';
</script>

<Navbar {siteName} {headerClass} {hamburgerClass} />
<Aside {asideClass}>
	<Nav {navClass} {navDivClass}>
		<h3 class="text-blue-100">Menu 1</h3>
		{#each lists as list}
			<SidebarList url={list.url} name={list.name} {sideBarListClass} />
		{/each}
	</Nav>
	<Nav {navClass} {navDivClass}>
		<h3 class="text-blue-100">Menu 2</h3>
		{#each lists2 as list}
			<SidebarList url={list.url} name={list.name} {sideBarListClass} />
		{/each}
	</Nav>
</Aside>
