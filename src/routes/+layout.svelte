<script>
	// import favicon from "$lib/assets/favicon.svg";
	import "../app.css";
	let { children } = $props();
	import StyledButton from "$lib/components/StyledButton.svelte";

	const backButton = [
		{
			href: "#back",
			icon: "fa-solid fa-arrow-left",
			ariaLabel: "Voltar",
		},
	];

	const archiveButtons = [
		{
			href: "#professional",
			label: "Profissional",
		},
		{
			href: "#personal",
			label: "Pessoal",
		},
	];

	const contactButtons = [
		{
			href: "https://www.github.com/vitor-n",
			target: "_blank",
			icon: "fa-brands fa-github",
			ariaLabel: "Github",
		},
		{
			href: "https://www.linkedin.com/in/vitor-do-nascimento",
			target: "_blank",
			icon: "fa-brands fa-linkedin",
			ariaLabel: "LinkedIn",
		},
		{
			href: "mailto: vitornascimento@proton.me",
			target: "_blank",
			icon: "fa-solid fa-envelope",
			ariaLabel: "Email",
		},
	];
</script>

<main
	class="mx-auto w-full px-8 md:px-0 md:w-2/3 lg:w-1/2 h-full relative gap-16 py-8 md:py-16 flex flex-col"
>
	<nav class="flex justify-center md:justify-end items-center gap-2">
		<StyledButton items={backButton} />
		<StyledButton items={archiveButtons} />
		<StyledButton items={contactButtons} />
	</nav>

	{@render children?.()}

	<footer
		class="flex mx-auto flex-col md:flex-row items-center gap-2 opacity-60"
	>
		<p class="text-base">Feito por mim</p>
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
