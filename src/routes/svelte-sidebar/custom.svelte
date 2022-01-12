<script>
	import { Sidebar } from '@codewithshin/svelte-sidebar';
	let lists = [
		{ url: 'svelte-sidebar', name: 'Svelte-sidebar Home' },
		{ url: 'svelte-sidebar/default', name: 'Sidebar Default' },
		{ url: 'svelte-sidebar/custom', name: 'Sidebar Custom Style' },
		{ url: 'svelte-sidebar/multi-default', name: 'Multi-menu Default' },
		{ url: 'svelte-sidebar/multi-custom', name: 'Multip-menu Custom Style' }
	];
	let siteName = 'Svelte-sidebar Custom Style';
	let headerClass = 'bg-red-200 py-3 px-10 items-center text-yellow-600 border-b-2';
	let asideClass = 'absolute w-auto h-full bg-purple-200 border-r-2 shadow-lg';
	let navClass = 'p-5 text-xl';
</script>

<Sidebar {lists} {siteName} {headerClass} {asideClass} {navClass} />
<main class="container mx-auto p-8">
	<h1>{siteName}</h1>
</main>
