<script lang="ts">
	import BindableRuneComponent from '../components/BindableRuneComponent.svelte';

	let parentCount = $state(0);
</script>

<div class="container mx-auto p-8">
	<h1 class="mb-4 text-3xl font-bold">Welcome to SvelteKit</h1>
	<p class="mb-8">
		Visit <a href="https://svelte.dev/docs/kit" class="text-blue-600 hover:underline"
			>svelte.dev/docs/kit</a
		> to read the documentation
	</p>

	<div class="mb-8">
		<BindableRuneComponent bind:count={parentCount} label="Parent Count" />
	</div>

	<div class="rounded-md border border-gray-200 p-4">
		<p class="mb-2 text-lg">Parent count: <span class="font-bold">{parentCount}</span></p>
		<button
			class="focus:ring-opacity-50 rounded-md bg-green-500 px-4 py-2 font-semibold text-white hover:bg-green-600 focus:ring-2 focus:ring-green-500 focus:outline-none"
			onclick={() => parentCount++}
		>
			Increment from Parent
		</button>
	</div>
</div>
