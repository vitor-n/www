<head>
	<meta charset="UTF-8" />
	<meta name="viewport" content="width=device-width, initial-scale=1.0" />
	<script src="https://unpkg.com/@tailwindcss/browser@4"></script>
	<link rel="stylesheet" href="//use.fontawesome.com/releases/v6.7.2/css/all.css" />
</head>

<main
	class="mx-auto w-full px-12 md:px-0 md:w-2/3 lg:w-1/2 h-full relative gap-16 py-18 flex flex-col"
>
	<nav class="flex justify-between">
		<a id="logo" href="/">
			<h2 class="text-3xl font-bold">Vitor do Nascimento</h2>
			<h4 class="text-base italic">Data Science Student</h4>
		</a>
		<div class="gap-5 flex items-center">
			<a href="https://github.com/vitor-n" target="_blank">
				<i class="fa-brands fa-github"></i>
			</a>
			<a href="https://linkedin.com/in/vitor-do-nascimento" target="_blank">
				<i class="fa-brands fa-linkedin"></i>
			</a>
			<a href="mailto:vitornascimento@proton.me" target="_blank">
				<i class="fa-solid fa-envelope"></i>
			</a>
		</div>
	</nav>

	<section>
		<h1 class="text-xl font-bold flex gap-2">Olá 👋</h1>
		<div class="text-base opacity-60">
			<p>
				Graduando em Ciência de Dados &amp; Inteligência Artificial pela Fundação Getulio Vargas
				(FGV), com sólida experiência em Machine Learning, Visualização de Dados e Análise
				Estatística. Atualmente, estou trabalhando de um projeto de pesquisa focado nas propriedades
				do Laplaciano de Feixes.
			</p>
		</div>
	</section>
	<section class="md:ml-5 flex flex-col gap-8">
		{#each { length: 3 } as _}
			<a href="/" class="flex flex-col gap-4 md:grid md:grid-cols-2 md:gap-x-16 md:items-center">
				<div class="contents md:flex md:flex-col md:gap-2">
					<h1 class="text-xl font-bold order-1 md:order-none">Modest</h1>
					<p class="text-base opacity-60 order-3 md:order-none">
						Lorem, ipsum dolor sit amet consectetur adipisicing elit. Totam unde autem accusantium
					</p>
					<div class="flex text-sm font-semibold items-center gap-2 order-4 md:order-none">
						Ver Mais
						<i class="fa-solid fa-arrow-right"></i>
					</div>
				</div>

				<img
					src="https://m.media-amazon.com/images/I/81VEl1TnKxL.jpg"
					class="w-90 h-40 object-cover rounded-xl order-2 md:order-none"
					alt=""
				/>
			</a>
		{/each}
	</section>
	<footer class="mx-auto flex flex-col md:flex-row gap-2 opacity-60">
		<p class="text-base">Feito por mim</p>
		<p class="hidden md:block">&bullet;</p>
		<a class="text-base font-bold" href="https://github.com/vitor-n/www" target="_blank">
			Source Code
		</a>
	</footer>
</main>
