<script lang="ts">
	import { AspectRatio } from '$lib/components/ui/aspect-ratio';
	import { Button } from '$lib/components/ui/button';

	type HeadersProps = {
		logoSrc?: string;
		links: Array<{ href: string; text: string }>;
	};

	const { logoSrc, links }: HeadersProps = $props();
</script>

<div class="top-header h-header flex items-center justify-between px-4">
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
	<div>
		<Button>resume</Button>
	</div>
</div>

<style lang="postcss">
	.top-header {
		@apply fixed left-0 right-0 top-0 z-50 bg-white shadow-md;
	}

	.head {
		@apply flex gap-4;
	}
</style>
