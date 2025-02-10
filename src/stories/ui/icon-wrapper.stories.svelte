<script module>
	import { defineMeta } from '@storybook/addon-svelte-csf';
	import SquareWrapper from '../../entities/icon/ui/square-wrapper.svelte';
	// import type { SquareWrapperProps } from "../../entities/icon/ui/square-wrapper.svelte";
	import { Linkedin } from 'lucide-svelte';

	const { Story } = defineMeta({
		title: 'Components/SquareWrapper',
		component: SquareWrapper,
		tags: ['autodocs']
	});
</script>

<Story name="basic" args={{ icon: Linkedin }} />
