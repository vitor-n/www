<script>
	/**
	 * @typedef  {Object} ButtonItem
	 * @property {string} href
	 * @property {string} [label]
	 * @property {string} [icon]
	 * @property {string} [ariaLabel]
	 * @property {string} [target]
	 */

	/** @type {ButtonItem[]} */
	export let items = [];
</script>

{#if items.length > 0}
	<div class="flex h-8 items-center rounded-xl bg-neutral-000 overflow-hidden">
		{#each items as item}
			<a
				href={item.href}
				target={item.target}
				aria-label={item.ariaLabel || item.label}
				class="flex h-full items-center justify-center px-3
                       transition-transform duration-200 focus:outline-none
                       hover:scale-110"
				class:hover:scale-115={item.icon}
			>
				{#if item.icon}
					<i class={item.icon}></i>
				{:else if item.label}
					<span class="text-sm font-medium">
						{item.label}
					</span>
				{/if}
			</a>
		{/each}
	</div>
{/if}
