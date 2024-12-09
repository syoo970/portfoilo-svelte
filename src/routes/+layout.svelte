<script lang="ts">
	import '../app.css';
	import { Headers } from '../widgets/Header';
	let { children } = $props();
</script>

<Headers
	links={[
		{ text: 'Home', href: '/' },
		{ text: 'About', href: '/about' },
		{ text: 'Contact', href: '/contact' }
	]}
/>
{@render children()}
