<script lang="ts">
	import SquareWrapper from '../../../entities/icon/ui/square-wrapper.svelte';
	import { type Icon as IconType } from 'lucide-svelte';

	type SnsBlockProps = {
		icons: Array<{
			icon: typeof IconType;
		}>;
	};

	let { icons }: SnsBlockProps = $props();
</script>

<div class="container">
	{#each icons as icon}
		<SquareWrapper icon={icon.icon} />
	{/each}
</div>

<style lang="postcss">
	.container {
		@apply flex items-center gap-2;
	}
</style>
