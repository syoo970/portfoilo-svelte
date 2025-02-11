<script lang="ts">
	import SquareWrapper from '../../../entities/icon/ui/square-wrapper.svelte';
	import type { Snippet } from 'svelte';
	import VelogLogo from '../../../entities/svg-images/ui/velog-logo.svelte';
	import Linkedin from 'lucide-svelte/icons/linkedin';
</script>

{#snippet rawicon(children: Snippet)}
	<div class="raw-wrapper">
		{@render children()}
	</div>
{/snippet}

<div class="container">
	<SquareWrapper classNames="z-1 bg-white dark:border-black dark:bg-black rounded-md">
		<Linkedin fill="currentColor" class="z-10" />
	</SquareWrapper>
	{@render rawicon(VelogLogo as unknown as Snippet)}
</div>

<style lang="postcss">
	.container {
		@apply flex items-center gap-2;
	}

	.raw-wrapper {
		@apply flex h-[42px] w-[42px];
	}
</style>
