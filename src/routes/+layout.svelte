<script>
	// import favicon from "$lib/assets/favicon.svg";
	import { onMount } from "svelte";
	import { animate, stagger } from "motion";

	import "../app.css";
	import StyledButton from "$lib/components/StyledButton.svelte";

	import {
		backButton,
		archiveButtons,
		contactButtons,
	} from "$lib/const.js";

	let { children } = $props();

	async function main() {
		await animate(
			"nav > *, #content > a > *, #content > p",
			{
				opacity: [0, 1],
				y: [20, 0],
				blur: [1, 0],
			},
			{
				delay: stagger(0.05),
			},
		);

		await animate(
			"#projects > a > div > *, #projects > a > img",
			{
				opacity: [0, 1],
				x: [-20, 0],
				blur: [1, 0],
			},
			{
				delay: stagger(0.05),
			},
		);

		await animate(
			"footer > *",
			{
				opacity: [0, 1],
				blur: [1, 0],
				y: [20, 0],
			},
			{
				delay: stagger(0.05),
			},
		);
	}

	onMount(main);
</script>

<main
	class="mx-auto w-full px-8 md:px-0 md:w-2/3 lg:w-1/2 h-full relative gap-16 py-8 md:py-16 flex flex-col"
>
	<nav class="flex justify-center md:justify-end items-center gap-2">
		<!-- <StyledButton items={backButton} /> -->
		<!-- <StyledButton items={archiveButtons} /> -->
		<StyledButton items={contactButtons} />
	</nav>

	{@render children?.()}

	<footer
		class="flex mx-auto flex-col md:flex-row items-center gap-2 opacity-60"
	>
		<p class="text-base">Feito por mim, Vitor</p>
		<p class="hidden md:block">&bullet;</p>
		<a
			class="text-base font-bold"
			href="https://github.com/vitor-n/www"
			target="_blank"
		>
			Source Code
		</a>
	</footer>
</main>
