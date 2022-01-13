<script>
	import { Sidebar } from '@codewithshin/svelte-sidebar';
	let lists = [
		{ url: 'svelte-sidebar-single', name: 'Home' },
		{ url: 'svelte-sidebar-single/about', name: 'About' }
	];
	let siteName = 'My demo';
</script>

<Sidebar {lists} {siteName} />
<div class="container mx-auto">
	<main class="p-8">
		<slot />
	</main>
</div>
