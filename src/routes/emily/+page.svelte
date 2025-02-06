<script>
	import { livros } from '$lib/emily.js';

	let filtrados = $state(livros.slice());
	let busca = $state('');

	function filtrar(event) {
		if (busca.length == 0) {
			filtrados = livros.slice();
		} else {
			filtrados = [];
			for (const livro of livros) {
				if (livro.gêneros.includes(busca.toLocaleLowerCase())) {
					filtrados.push(livro);
				}
				if (livro.nome.toLowerCase().includes(busca.toLocaleLowerCase())) {
					filtrados.push(livro);
				}
			}
		}
	}
</script>

<div class="barra">
	<nav class="navbar bg-body-tertiary">
		<div class="container-fluid">
			<a class="navbar-brand" href=".">
				<img src="book.svg" alt="." width="30" height="24" class="d-inline-block align-text-top" />
				<b>BlogBook</b>
			</a>
		<nav class="navbar navbar-expand-lg bg-body-tertiary">
			<div class="container-fluid">
				<div class="collapse navbar-collapse" id="navbarTogglerDemo02">
					<form class="d-flex" role="search">
						<input
							class="btn btn-dark"
							type="Search"
							placeholder="livro.."
							aria-label="Search"
                            bind:value={busca}
                            oninput={filtrar}
						/>
					</form>
				</div>
			</div>
		</nav>
	</div>
</div>
<br />
<br />
<div class=" d-flex justify-content-center">
	<div class="card mb-3" style="max-width: 800px;">
		<div class="row g-0">
			<div class="col-md-6">
				<img src="emily.png" class="img-fluid rounded-start" alt="..." />
			</div>
			<div class="col-md-6">
				<div class="card-body">
					<h5 class="card-title"><b>Emily Henry</b></h5>
					<h7 class="card-title"><b>@emilyhenrywrites</b></h7>
					<br />
					<br />
					<p class="card-text">
						Emily Henry é uma escritora norte-americana e best-seller do New York Times. Seu livro
						de estreia foi “O amor que partiu o mundo”, mas ela ficou realmente famosa com seu
						primeiro romance para adultos, “Leitura de Verão“, em 2020.
					</p>
					<p>
						A autora tem uma forma especial de trazer reflexões sobre os pequenos momentos do dia a
						dia, mesclando lições sobre empatia e momentos de acolhimento. E, embora os temas
						tratados possam resultar em um tempo maior para absorver todos os acontecimentos, sua
						escrita ainda é fluida e envolvente.
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
<div class="row g-4">
	{#each filtrados as livro}
		<div class="col d-flex align-items-center">
			<div class="border p-2">
				<img style="width:200px" src={livro.imagem} alt="..." />
			</div>
		</div>
	{/each}
</div>

<p>emily</p>

<style>
	.haipados {
		text-align: center;
		color: rgb(0, 0, 0);
	}
</style>
