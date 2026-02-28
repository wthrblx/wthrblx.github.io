<script lang="ts">
	import './layout.css';
	import favicon from '$lib/assets/favicon.svg';
	import Header from '$lib/components/ui/Header.svelte';

	import '@fontsource/titillium-web/200.css';
	import '@fontsource/titillium-web/300.css';
	import '@fontsource/titillium-web/400.css';
	import '@fontsource/titillium-web/600.css';
	import '@fontsource/titillium-web/700.css';
	import '@fontsource/titillium-web/900.css';
	import '@fontsource/titillium-web/200-italic.css';
	import '@fontsource/titillium-web/300-italic.css';
	import '@fontsource/titillium-web/400-italic.css';
	import '@fontsource/titillium-web/600-italic.css';
	import '@fontsource/titillium-web/700-italic.css';

	let { children } = $props();
</script>

<svelte:head>
	<title>Welcome To Hell</title>
	<link rel="icon" href={favicon} />
</svelte:head>

<Header />

<main>
	{@render children()}
</main>
