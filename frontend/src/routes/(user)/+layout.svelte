<script lang="ts">
	import '../../app.css';
	let { children } = $props();
</script>

<div class="h-screen flex items-center justify-center">
	<div class="w-[30%]">
		<div class="p-4 bg-gray-100 rounded-lg shadow-lg">
			{@render children()}
		</div>
	</div>
</div>
