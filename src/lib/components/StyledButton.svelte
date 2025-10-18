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

<div class="flex rounded-lg bg-neutral-000 overflow-hidden">
	{#if items.length === 1}
		{@const item = items[0]}

		<a
			href={item.href}
			target={item.target}
			aria-label={item.ariaLabel || item.label}
			class="hover:scale-110 duration-200 focus:outline-none"
			class:hover:scale-115={item.icon}
			class:p-2.5={item.icon}
			class:py-2={item.label}
			class:px-4={item.label}
		>
			{#if item.icon}
				<i class={item.icon}></i>
			{:else if item.label}
				<span class="text-sm font-medium">
					{item.label}
				</span>
			{/if}
		</a>
	{:else if items.length > 1}
		{#each items as item, i}
			{#if i > 0}
				<div class="w-[0px] bg-black"></div>
			{/if}

			<a
				href={item.href}
				target={item.target}
				aria-label={item.ariaLabel || item.label}
				class="hover:scale-110 transition duration-200 focus:outline-none"
				class:hover:scale-115={item.icon}
				class:px-4={item.label}
				class:py-2={item.label}
				class:text-sm={item.label}
				class:font-medium={item.label}
				class:p-2.5={item.icon}
				class:flex={item.icon}
				class:items-center={item.icon}
				class:justify-center={item.icon}
			>
				{#if item.icon}
					<i class={item.icon}></i>
				{:else if item.label}
					{item.label}
				{/if}
			</a>
		{/each}
	{/if}
</div>
