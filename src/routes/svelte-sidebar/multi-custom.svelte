<script>
	import { Aside } from '@codewithshin/svelte-sidebar';
	import { Nav } from '@codewithshin/svelte-sidebar';
	import { SidebarList } from '@codewithshin/svelte-sidebar';
	import { Navbar } from '@codewithshin/svelte-sidebar';
	let siteName = 'Svelte-sidebar Multiple-menu Custome Style';
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
	let navClass = 'pt-2 px-12 text-xl';
	let navDivClass = 'pb-10';
	let sideBarListClass = 'border-b border-red-400 mb-2 px-4';
	let hamburgerClass =
		'text-blue-500 hover:text-blue-700 cursor-pointer mr-4 border-none focus:outline-none';
	let asideClass = 'absolute w-auto h-full bg-green-200 border-r-2 shadow-lg';
	let headerClass = 'bg-yellow-200 py-3 px-10 items-center text-red-600 border-b-2';
</script>

<Navbar {siteName} {hamburgerClass} {headerClass} />
<Aside {asideClass}>
	<Nav {navClass} {navDivClass}>
		<h3>Menu 1</h3>
		{#each lists as list}
			<SidebarList url={list.url} name={list.name} {sideBarListClass} />
		{/each}
	</Nav>
	<Nav {navClass}>
		<h3>Menu 2</h3>
		{#each lists2 as list}
			<SidebarList url={list.url} name={list.name} {sideBarListClass} />
		{/each}
	</Nav>
</Aside>

<main class="container mx-auto p-8">
	<h1>{siteName}</h1>
</main>
