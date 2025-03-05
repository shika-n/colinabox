<script>
let res = $state("Not yet");
async function ping() {
	const pingRes = await fetch("http://localhost:9000/ping");
	return await pingRes.json();
}
</script>

<div>
	Test
	<br>
	{#if typeof res == "string"}
		{res}
	{:else}
		{#await res}
			Fetching...
		{:then val}
			{console.log(val)}
			{val.message}
		{:catch err}
			Error: {err}
		{/await}
	{/if}
	<br>
	<button onclick={() => res = ping()} class="bg-blue-500">Fetch</button>
</div>
