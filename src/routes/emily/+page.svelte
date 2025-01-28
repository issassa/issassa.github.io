<script>
	import Page from "../+page.svelte";

</script>
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
					<h5 class="card-title"><b>Emily Henry</b></h5>
                    <h7 class="card-title"><b>@emilyhenrywrites</b></h7>
                    <br>
                    <br>
					<p class="card-text">
						Emily Henry é uma escritora norte-americana e best-seller do New York Times. Seu livro de estreia foi “O amor que partiu o mundo”, mas ela ficou realmente famosa com seu primeiro romance para adultos, “Leitura de Verão“, em 2020.
                        <p>A autora tem uma forma especial de trazer reflexões sobre os pequenos momentos do dia a dia, mesclando lições sobre empatia e momentos de acolhimento. E, embora os temas tratados possam resultar em um tempo maior para absorver todos os acontecimentos, sua escrita ainda é fluida e envolvente.
                        <p>Nos últimos anos, a escritora tem publicado um novo livro de romance a cada ano. Aqui nesse post, vou te mostrar todos os livros de Emily Henry por ordem de lançamento, suas próximas publicações e mais curiosidades sobre ela e seus livros.
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

<p>emily</p>

<style>
	.haipados {
		text-align: center;
		color: rgb(137, 40, 228);
	}
</style>
