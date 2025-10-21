<script>
	export let items = [];
</script>

<div class="flex flex-row flex-wrap gap-2">
	{#each items as item}
		<span
			class="text-sm font-bold bg-neutral-700 text-white rounded-xl px-2.5 py-0.5"
		>
			{item}
		</span>
	{/each}
</div>
