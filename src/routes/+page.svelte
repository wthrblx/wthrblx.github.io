<script>
	import { Button } from '$lib/components/ui/button';
	import Logo from '$lib/components/ui/Logo.svelte';
</script>

<section
	id="hero"
	class="flex w-full flex-col items-center justify-center gap-2 overflow-hidden pt-50 pb-25 text-center text-balance"
>
	<img
		src="/media/terrain.png"
		alt="Landscape view of Chapter 1 from the sea"
		class="absolute top-0 left-0 -z-1 h-full w-full object-cover object-center brightness-67"
	/>
	<h1 class="sr-only">Welcome To Hell</h1>
	<Logo class="w-full max-w-90" />
	<p class="heading text-6xl">Chapter 1</p>
	<p class="mb-4 text-4xl">Launching in 2026</p>
	<Button variant="default">Follow Development</Button>
</section>

<section class="w-full gap-4 bg-background px-40 py-20 text-center">
	<div class="container mx-auto grid grid-cols-1 gap-10 md:grid-cols-2">
		<h2 class="sr-only">About Welcome To Hell</h2>
		<span class="heading inline-flex flex-col items-center gap-2 text-xl">
			A little bit about <Logo class="w-full max-w-100" />
		</span>
		<div class="flex flex-col gap-2 text-left">
			<span class="heading text-xl">You're our Pilot.</span>
			<p>
				Welcome To Hell is an experimental tower-obby game focused on fresh gameplay and true-to-its-roots inspirations,
				all woven together with a rewarding narrative.
			</p>
			<p>
				Endless towers pierce the sky, rising from rosefields long scorched. Whatever ended civilization is over, but
				its consequences remain. You wished it wasn't this hard.
			</p>
		</div>
	</div>
</section>
