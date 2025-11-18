<script>
	export let title;
	export let description;
	export let imageUrl;
	export let link = "/";
</script>

<a href="{link}" class="flex flex-col gap-4 md:grid md:grid-cols-2 md:gap-x-16 md:items-center">
	<div class="contents md:flex md:flex-col md:gap-2">
		<h1 class="text-xl font-bold order-1 md:order-none">
			{title}
		</h1>

		<p class="text-base text-neutral-600 order-3 md:order-none">
			{description}
		</p>

		<div class="group flex text-sm font-semibold items-center gap-2 order-4 md:order-none">
			Ver Mais
			<i class="fa-solid fa-arrow-right"></i>
		</div>
	</div>

	<img
		src={imageUrl}
		alt={title}
		class="w-90 h-40 object-cover rounded-xl order-2 md:order-none"
	/>
</a>
