<script>
	import { Sidebar } from '@codewithshin/svelte-sidebar';
	let lists = [
		{ url: 'svelte-sidebar-single2', name: 'Home' },
		{ url: 'svelte-sidebar-single2/about', name: 'About' }
	];
	let siteName = 'Svelte-Sidebar';
	let hamburgerClass =
		'text-white hover:text-gray-500 cursor-pointer mr-4 border-none focus:outline-none';
	let headerClass = 'bg-gray-700 py-3 px-10 items-center text-white border-b-2';
	let asideClass = 'absolute w-auto h-full bg-gray-700 text-white border-r-2 shadow-lg';
	let navClass = 'p-5 text-xl';
	let navDivClass = 'pb-10';
	let sideBarListClass = 'border-b border-gray-100 mb-2 px-4 hover:text-gray-500';
</script>

<Sidebar
	{lists}
	{siteName}
	{headerClass}
	{asideClass}
	{navClass}
	{navDivClass}
	{hamburgerClass}
	{sideBarListClass}
/>
<div class="container mx-auto">
	<main class="p-8">
		<slot />
	</main>
</div>
