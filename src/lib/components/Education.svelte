<script>
	export let education = {};
</script>

<div class="flex flex-row items-center justify-between">
	<div class="flex flex-row items-center gap-4">
		<img class="w-16 rounded-full border-1 border-neutral-300" src={education.img} alt="" />
		<div>
			<h1 class="font-bold">{education.name}</h1>
			<p>{education.course}</p>
		</div>
	</div>

	<span>{education.from} &hyphen; {education.to}</span>
</div>
