<script lang="ts">
	import '../app.css';
	import { Headers } from '../widgets/Header';
	let { children } = $props();
</script>

<Headers
	logoSrc="/logo.png"
	links={[
		{ text: 'Home', href: '/' },
		{ text: 'About', href: '/about' },
		{ text: 'Contact', href: '/contact' }
	]}
/>
<div class="h-header"></div>
<main class="p-2">
	{@render children()}
</main>
