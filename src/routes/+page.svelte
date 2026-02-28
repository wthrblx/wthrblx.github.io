<script>
	import { Button } from '$lib/components/ui/button';
	import Logo from '$lib/components/ui/Logo.svelte';
</script>

<section
	id="hero"
	class="flex min-h-[60vh] w-full flex-col items-center justify-center gap-2 pt-50 pb-25 text-center text-balance"
>
	<h1 class="sr-only">Welcome To Hell</h1>
	<Logo class="mb-4 w-full max-w-140" />
	<p class="heading text-5xl">A Star Upon A Child</p>
	<p class="lowercase">The First Chapter, Releasing in 2026</p>
	<Button variant="default" class="lg">Follow Development</Button>
</section>

<section class="w-full gap-4 bg-red-950 px-40 py-20 text-center">
	<div class="container mx-auto grid grid-cols-1 gap-10 md:grid-cols-2">
		<h2 class="sr-only">About Welcome To Hell</h2>
		<span class="heading inline-flex flex-col items-center gap-2 text-xl">
			A little bit about <Logo class="w-full max-w-100" />
		</span>
		<div class="flex flex-col gap-2 text-left">
			<span class="heading text-xl">You're our Pilot.</span>
			<p>
				Welcome To Hell is an experimental tower-obby game focused on fresh gameplay and
				true-to-its-roots inspirations, all woven together with a rewarding narrative.
			</p>
			<p>
				Endless towers pierce the sky, rising from rosefields long scorched. Whatever ended
				civilization is over, but its consequences remain. You wished it wasn't this hard.
			</p>
		</div>
	</div>
</section>
