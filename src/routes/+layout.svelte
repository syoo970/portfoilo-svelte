<script lang="ts">
	import '../app.css';
	import { Headers } from '../widgets/Header';
	import { ModeWatcher } from 'mode-watcher';

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
<main class="relative top-[var(--header-height)] p-4">
	{@render children()}
</main>
<ModeWatcher></ModeWatcher>
