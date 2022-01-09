<script>
  import Logo from "./Logo.svelte";
  import Hamburger from "./Hamburger.svelte";

  export let sidebar = false;
</script>

<header class="bg-gray-200 py-3 px-10 items-center text-gray-600 border-b-2">
  <nav class="flex">
    <Hamburger bind:open={sidebar} />
    <Logo />
  </nav>
</header>
