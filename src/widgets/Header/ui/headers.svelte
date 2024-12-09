<script lang="ts">
	import { goto } from '$app/navigation';

	type HeadersProps = {
		logoSrc?: string;
		links: Array<{ href: string; text: string }>;
	};

	const { logoSrc, links }: HeadersProps = $props();
</script>

<div class="head">
	<div></div>
	<div class="head">
		{#each links as link (link.href)}
			<a href={link.href} aria-label={link.text}>{link.text}</a>
		{/each}
	</div>
</div>

<style lang="postcss">
	.head {
		@apply flex gap-2;
	}
</style>
