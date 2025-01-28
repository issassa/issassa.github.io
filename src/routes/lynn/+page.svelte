<nav class="navbar bg-dark border-bottom border-body" data-bs-theme="dark">
	<div class="container-fluid">
		<a class="navbar-brand" href=".">
			<img
				src="/docs/5.3/assets/brand/bootstrap-logo.svg"
				alt=""
				width="30"
				height="24"
				class="d-inline-block align-text-top"
			/>
			<b>BiblioBella</b>
		</a>
		<nav class="navbar navbar-expand-lg bg-body-tertiary">
			<div class="container-fluid">
				<div class="collapse navbar-collapse" id="navbarTogglerDemo02">
					<form class="d-flex" role="search">
						<input
							class="btn btn-dark"
							type="Search"
							placeholder="nome do livro.."
							aria-label="Search"
						/>
						<button class="btn btn-dark" type="button">ok</button>
					</form>
				</div>
			</div>
		</nav>
	</div>
</nav>
<br />
<br />
<div class=" d-flex justify-content-center">
	<div class="card mb-3" style="max-width: 540px;">
		<div class="row g-0">
			<div class="col-md-4">
				<img src="..." class="img-fluid rounded-start" alt="..." />
			</div>
			<div class="col-md-8">
				<div class="card-body">
					<h5 class="card-title"><b>Lynn Painter</b></h5>
					<h7 class="card-title"><b>@lynnpainterbooks</b></h7>
					<br />
					<br />
					<p class="card-text">
						É autora best-seller de comédias românticas para leitores jovens e adultos. Ela mora com
						o marido e os filhos em Nebraska, nos Estados Unidos, e tem uma coluna no jornal Omaha
						World-Herald, onde fala sobre família e comportamento parental, apesar de ser o oposto
						de uma mãe exemplar. Quando não está atrás das crianças, Lynn gosta de ler, escrever,
						beber energético e assistir a filmes de comédia romântica. É autora de Melhor do que nos
						filmes, Amor por engano, Mil vezes amor e Apostando no amor, publicados pela Intrínseca.
					</p>
				</div>
			</div>
		</div>
	</div>
</div>
<br />
<br />
<div class="haipados">
	<h2><b>Os mais queridinhos</b></h2>
</div>
<br />
<br />
<div class="row row-cols-1 row-cols-md-3 g-4">
	{#each livros as livro}
		<div class="col">
			<div class="card">
				<img src={livro.imagem} class="card-img-top" alt="..." />
			</div>
		</div>
	{/each}
</div>
<div class="row row-cols-1 row-cols-md-3 g-4">
	<div class="col">
		<div class="card">
			<img src="..." class="card-img-top" alt="..." />
		</div>
	</div>
	<div class="col">
		<div class="card">
			<img src="..." class="card-img-top" alt="..." />
		</div>
	</div>
	<div class="col">
		<div class="card">
			<img src="..." class="card-img-top" alt="..." />
		</div>
	</div>
	<div class="col">
		<div class="card">
			<img src="..." class="card-img-top" alt="..." />
		</div>
	</div>
	<div class="col">
		<div class="card">
			<img src="..." class="card-img-top" alt="..." />
		</div>
	</div>
	<div class="col">
		<div class="card">
			<img src="..." class="card-img-top" alt="..." />
		</div>
	</div>
	<div class="col">
		<div class="card">
			<img src="..." class="card-img-top" alt="..." />
		</div>
	</div>
	<div class="col">
		<div class="card">
			<img src="..." class="card-img-top" alt="..." />
		</div>
	</div>
	<div class="col">
		<div class="card">
			<img src="..." class="card-img-top" alt="..." />
		</div>
	</div>
</div>

<p>lynn</p>

<style>
	.haipados {
		text-align: center;
		color: rgb(137, 40, 228);
	}
</style>
