<script lang="ts">
	import * as Sheet from '$lib/components/ui/sheet';
	import { Button } from '$lib/components/ui/button';
	import { Menu } from 'lucide-svelte/icons';
</script>

<Sheet.Root>
	<Sheet.Trigger asChild let:builder>
		<Button
			size="icon"
			builders={[builder]}
			class="bg-white text-primary hover:bg-transparent hover:font-bold sm:hidden"
		>
			<Menu size={24} class="hover:stroke-[3]" />
		</Button>
	</Sheet.Trigger>
	<Sheet.Content side="left"></Sheet.Content>
</Sheet.Root>

<style lang="postcss"></style>
