<script lang="ts">
	let { count = $bindable(), label }: { count: number; label: string } = $props();
</script>

<div class="rounded-md border border-gray-300 p-4 shadow-sm">
	<p class="mb-2 text-lg">
		{label}: <span class="font-bold text-blue-600">{count}</span>
	</p>
	<button
		class="focus:ring-opacity-50 rounded-md bg-blue-500 px-4 py-2 font-semibold text-white hover:bg-blue-600 focus:ring-2 focus:ring-blue-500 focus:outline-none"
		onclick={() => count++}
	>
		Increment from Child
	</button>
</div>
