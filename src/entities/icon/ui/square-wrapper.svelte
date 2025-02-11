<script lang="ts">
	// import { type Icon as IconType } from 'lucide-svelte';
	import { cn } from '@/utils';
	import type { Snippet } from 'svelte';

	export type SquareWrapperProps = {
		children: Snippet;
		classNames?: string;
	};

	let { classNames, children }: SquareWrapperProps = $props();
</script>

<div class={cn('icon-wrapper icon-hover', classNames)}>
	{@render children()}
</div>

<style lang="postcss">
	.icon-wrapper {
		@apply flex items-center justify-center border border-slate-600 bg-transparent p-2 dark:border-black dark:bg-black;
	}

	.icon-hover {
		@apply cursor-pointer hover:bg-black hover:text-white;
	}
</style>
