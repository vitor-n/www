<script>
	import Card from "$lib/components/Card.svelte";
</script>

<section>
	<div id="content" class="flex flex-col gap-10">
		<a href="/">
			<h1 class="text-4xl font-bold">Olá, eu sou o Vitor!</h1>
			<h4 class="text-base italic opacity-60">Graduando em Ciência de Dados &amp; IA</h4>
		</a>

		<p class="text-base text-neutral-600">
			Graduando em Ciência de Dados &amp; Inteligência Artificial pela
			FGV - RJ, com sólido conhecimento em
			Machine Learning, Visualização de Dados e Análise de Dados.
			Atualmente, estou trabalhando em um projeto de pesquisa (bolsista PIBIC) focado
			elaboração de Redes Neurais Geometricas, com foco em Sheaf Neural
			Networks.
		</p>
	</div>
</section>

<section id="projects" class="md:ml-5 flex flex-col gap-8">
	{#each { length: 3 } as _}
		<Card
			title="Modest"
			description="Lorem, ipsum dolor sit amet consectetur adipisicing elit. Totam unde autem accusantium"
			imageUrl="https://m.media-amazon.com/images/I/81VEl1TnKxL.jpg"
			link="/"
		/>
	{/each}
</section>
