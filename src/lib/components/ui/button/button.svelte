<script lang="ts" module>
	import { cn, type WithElementRef } from '$lib/utils';
	import type { HTMLAnchorAttributes, HTMLButtonAttributes } from 'svelte/elements';
	import { type VariantProps, tv } from 'tailwind-variants';

	export const buttonVariants = tv({
		base: "after:transition-all button border-primary-foreground/67 border-2 rounded-xs relative inline-flex shrink-0 items-center justify-center gap-2 font-semibold whitespace-nowrap transition-all outline-none focus-visible:ring-[3px] disabled:pointer-events-none disabled:opacity-50 aria-disabled:pointer-events-none aria-disabled:opacity-50 [&_svg]:pointer-events-none [&_svg]:shrink-0 [&_svg:not([class*='size-'])]:size-4",
		variants: {
			variant: {
				default: 'text-heading bg-wth-ash hover:bg-wth-ash shadow-xs',
			},
			size: {
				default: 'h-10 px-4 has-[>svg]:px-3',
			},
		},
		defaultVariants: {
			variant: 'default',
			size: 'default',
		},
	});

	export type ButtonVariant = VariantProps<typeof buttonVariants>['variant'];
	export type ButtonSize = VariantProps<typeof buttonVariants>['size'];

	export type ButtonProps = WithElementRef<HTMLButtonAttributes> &
		WithElementRef<HTMLAnchorAttributes> & {
			variant?: ButtonVariant;
			size?: ButtonSize;
		};
</script>

<script lang="ts">
	let {
		class: className,
		variant = 'default',
		size = 'default',
		ref = $bindable(null),
		href = undefined,
		type = 'button',
		disabled,
		children,
		...restProps
	}: ButtonProps = $props();
</script>

{#if href}
	<a
		bind:this={ref}
		data-slot="button"
		class={cn(buttonVariants({ variant, size }), className)}
		href={disabled ? undefined : href}
		aria-disabled={disabled}
		role={disabled ? 'link' : undefined}
		tabindex={disabled ? -1 : undefined}
		{...restProps}
	>
		{@render children?.()}
	</a>
{:else}
	<button
		bind:this={ref}
		data-slot="button"
		class={cn(buttonVariants({ variant, size }), className)}
		{type}
		{disabled}
		{...restProps}
	>
		{@render children?.()}
	</button>
{/if}

<style>
	.button::after {
		--button-padding: 6px;

		content: '';
		display: block;

		position: absolute;

		width: calc(100% - var(--button-padding));
		height: calc(100% - var(--button-padding));
		margin: auto;

		border-width: 12px;
		border-style: solid;
		border-image: url('/media/ui/corners-pattern.svg');
		border-image-slice: 15;
		border-image-repeat: round;
		opacity: 33.33%;
	}

	.button:hover::after {
		--button-padding: 2px;
	}

	.button:active::after {
		--button-padding: 4px;
	}
</style>
