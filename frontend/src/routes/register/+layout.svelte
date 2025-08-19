<script lang="ts">
	import '../../app.css';
	let { children } = $props();
</script>

<div class="flex">
	<div class="p-2 flex-grow">
		{@render children()}
	</div>
</div>
