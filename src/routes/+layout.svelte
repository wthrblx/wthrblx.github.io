<script lang="ts">
	import './layout.css';
	import favicon from '$lib/assets/favicon.svg';
	import Header from '$lib/components/ui/Header.svelte';

	import '@fontsource-variable/merriweather/standard.css';
	import '@fontsource-variable/inter/standard.css';

	let { children } = $props();
</script>

<svelte:head>
	<title>Welcome To Hell</title>
	<link rel="icon" href={favicon} />
</svelte:head>

<Header />

<main class="bg-black text-white">
	{@render children()}
</main>
