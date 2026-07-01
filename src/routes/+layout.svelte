<script lang="ts">
	import "../app.scss";
	// import favicon from '$lib/assets/favicon.svg';
	import { page } from '$app/state';

	let { children } = $props();
	const currentPath = $derived(page.url.pathname);
</script>

<!-- <svelte:head><link rel="icon" href={favicon} /></svelte:head> -->

<header class="bg-blue-300 flex justify-between p-4 drop-shadow-md sticky">
	<a href="/" class="text-center content-center text-3xl text-black hover:text-white transition-colors">羽冬</a>
	<nav class="flex *:px-4">
		{#snippet link(path: string, name: string)}
			{#if path === currentPath}
			<div class="text-center content-center text-2xl text-black font-bold transition-colors">{name}</div>
			{:else}
			<a href={path} class="text-center content-center text-2xl text-black hover:text-white transition-colors">{name}</a>
			{/if}
		{/snippet}
		{@render link("/", "主頁")}
		{@render link("/VESS", "原體生存")}
	</nav>
</header>

<main class="grow">
	{@render children()}
</main>
