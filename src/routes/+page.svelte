<script>
	import Card from "$lib/components/Card.svelte";
</script>

<section>
	<div id="content" class="flex flex-col gap-10">
		<a href="/">
			<h4 class="text-base italic opacity-60">Cientista de Dados</h4>
			<h1 class="text-4xl font-bold">Olá, eu sou o Vitor</h1>
		</a>

		<p class="text-base opacity-60">
			Graduando em Ciência de Dados &amp; Inteligência Artificial pela
			Fundação Getulio Vargas (FGV), com sólida experiência em Machine
			Learning, Visualização de Dados e Análise Estatística. Atualmente,
			estou trabalhando de um projeto de pesquisa focado nas propriedades
			do Laplaciano de Feixes.
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
