<script>
	const checkStatus = async () => {
		const {
			data: { session }
		} = await browser.runtime.sendMessage({ action: 'getSession' });
		console.log('session', session);
	};
</script>

<h1>Welcome to SvelteKit</h1>
<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>
