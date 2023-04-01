<script>
	import { onMount } from 'svelte';

	const checkStatus = async () => {
		const {
			data: { session }
		} = await window.chrome.runtime.sendMessage({ action: 'getSession' });
		console.log('session', session);
	};

	onMount(() => {
		checkStatus();
	});
</script>

<h1>Welcome to SvelteKit</h1>
<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>
