<script lang="ts">
	import { type Icon as IconType } from 'lucide-svelte';
	import { cn } from '@/utils';

	export type SquareWrapperProps = {
		icon: typeof IconType;
		classNames?: string;
	};

	let { icon: Icon, classNames }: SquareWrapperProps = $props();
</script>

<div class={cn('icon-wrapper icon-hover', classNames)}>
	<Icon />
</div>

<style lang="postcss">
	.icon-wrapper {
		@apply flex items-center justify-center border border-slate-600 p-2;
	}

	.icon-hover {
		@apply cursor-pointer hover:bg-black hover:text-white;
	}
</style>
