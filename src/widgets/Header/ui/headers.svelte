<script lang="ts">
	import { AspectRatio } from '$lib/components/ui/aspect-ratio';
	import { Button } from '$lib/components/ui/button';
	import DarkToggleBtn from './dark-toggler.svelte';
	import { Download } from 'lucide-svelte/icons';
	import ResponsiveHeader from './responsive-header.svelte';

	type HeadersProps = {
		logoSrc?: string;
		links: Array<{ href: string; text: string }>;
	};

	const { logoSrc, links }: HeadersProps = $props();
</script>

<div class="top-header flex h-header items-center justify-between bg-white px-4 dark:bg-inherit">
	<ResponsiveHeader></ResponsiveHeader>
	<div class="flex w-[100px] items-center justify-center">
		<AspectRatio ratio={16 / 9} class="flex items-center justify-center">
			<img src={logoSrc} alt="logo" class="object-cover" />
		</AspectRatio>
	</div>
	<div class="head">
		{#each links as link (link.href)}
			<a href={link.href} aria-label={link.text} class="font-paperlogy">{link.text}</a>
		{/each}
	</div>
	<div class="head">
		<Button class="resume-btn gap-[6px]">
			resume
			<Download size={16}></Download>
		</Button>
		<DarkToggleBtn></DarkToggleBtn>
	</div>
</div>

<style lang="postcss">
	.top-header {
		@apply fixed left-0 right-0 top-0 z-50 shadow-md;
	}

	.head {
		@apply flex gap-4 max-sm:hidden;
	}

	.resume-btn {
		@apply flex items-center justify-center text-[14px];
	}
</style>
