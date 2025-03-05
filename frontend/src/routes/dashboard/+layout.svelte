<script lang="ts">
	import '../../app.css';
	import MenuItem from "./MenuItem.svelte";
	let { children } = $props();
</script>

<div class="flex">
	<div class="h-screen min-w-60 flex flex-col justify-between divide-y bg-neutral-800 text-white border-r-4 border-slate-500">
		<div class="flex flex-col divide-y">
			<h1 class="p-4 text-center text-2xl">ColinaBox</h1>
			<MenuItem text="Home" selected=true />
			<MenuItem text="Stats" />
			<MenuItem text="View" />
			<MenuItem text="Insert" />
		</div>
		<div class="flex flex-col divide-y">
			<MenuItem text="Settings" />
			<MenuItem text="Logout" extraClass="font-bold text-rose-400" />
		</div>
	</div>
	<div class="p-2 flex-grow">
		{@render children()}
	</div>
</div>
