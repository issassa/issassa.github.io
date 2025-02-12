<script>
	import CartaMagic from '$lib/components/CartaMagic.svelte';
	import { cards } from '$lib/data.js';
	import { goto } from '$app/navigation';
	import { livros } from '$lib/ofc.js';

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
	<nav class="navbar" style="background-color: #f2d6f7;">
		<div class="container-fluid">
			<a class="navbar-brand" href=".">
				<img src="book.svg" alt="." width="30" height="24" class="d-inline-block align-text-top" />
				<b>BlogBook</b>
			</a>
			<nav class="navbar navbar-expand-lg">
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
	</nav>
</div>
<div class="mb-3">
	<img src="fotocapaofcl.png" class="banner" alt="..." />
</div>
<br />
<br />
<br />
<div class="autorpreferido">
	<h1><b>Autoras Favoritas</b></h1>
</div>
<br />
<div class=" d-flex justify-content-center">
	<div class="card mb-3" style="max-width: 700px;">
		<div class="row g-0">
			<div class="col-md-6">
				<img
					src="sarah.png"
					class="img-fluid rounded-start"
					alt="..."
					width="600px"
					height="990px"
				/>
			</div>
			<div class="col-md-6">
				<div class="card-body" style="background-color: ;">
					<h5 class="card-title"><b>Sarah Adams</b></h5>
					<h7 class="card-title"><b>@authorsarahadams</b></h7>
					<br />
					<br />
					<p class="card-text">
						Nascida e criada em Nashville TN, Sarah Adams ama sua família, dias quentes e fazer as
						pessoas sorrirem.
					</p>
					<p>
						Sarah sonha em ser escritora desde menina, mas finalmente escreveu seu primeiro romance
						quando suas filhas estavam cochilando e ela não tinha mais desculpas para adiar.
					</p>
					<p>Blog da autora: <a href="https://www.authorsarahadams.com/">Sarah Adams</a></p>
				</div>
			</div>
		</div>
	</div>
</div>
<br />
<br />
<div class=" d-flex justify-content-center">
	<div class="card mb-3" style="max-width: 800px;">
		<div class="row g-0">
			<div class="col-md-6">
				<img
					src="emily.png"
					class="img-fluid rounded-start"
					alt="..."
					width="800px"
					height="990px"
				/>
			</div>
			<div class="col-md-6">
				<div class="card-body">
					<h5 class="card-title"><b>Emily Henry</b></h5>
					<h7 class="card-title"><b>@emilyhenrywrites</b></h7>
					<br />
					<br />
					<p class="card-text">
						Emily Henry é uma escritora norte-americana e best-seller do New York Times. Seu livro
						de estreia foi “O amor que partiu o mundo”.
					</p>
					<p>
						A autora tem uma forma especial de trazer reflexões sobre os pequenos momentos do dia a
						dia, mesclando lições sobre empatia e momentos de acolhimento. E, embora os temas
						tratados possam resultar em um tempo maior para absorver todos os acontecimentos, sua
						escrita ainda é fluida e envolvente.
					</p>
					<p>Blog da autora: <a href="https://www.emilyhenrybooks.com/">Emily Henry</a></p>
				</div>
			</div>
		</div>
	</div>
</div>
<br />

<br />
<br />
<br />
<div class="livropreferido">
	<h1><b>Livros Favoritos</b></h1>
</div>
<br />
<br />
<div class="foto">
	<div class="row g-4">
		{#each filtrados as livro}
			<div class="col d-flex align-items-center">
				<div class="border p-1">
					<a href={livro.url}><img style="width:335px" src={livro.imagem} alt="..." /> </a>
				</div>
			</div>
		{/each}
	</div>
</div>
<svelte:head>
	<style>
		body {
			background-color: #f2d6f7;
		}
	</style>
</svelte:head>

<style>
	.livropreferido {
		font-family: cursive;
		text-align: center;
		color: #000000;
	}
	.autorpreferido {
		font-family: cursive;
		text-align: center;
		color: rgb(0, 0, 0);
	}
	.barra {
		color: #ffffff;
	}
	.foto {
		text-align: center;
	}
	.banner {
		/* ocupa 90% da tela */
		max-width: 100vw;
		max-height: 100vh;

		/* centraliza */
		display: block;
		margin-left: auto;
		margin-right: auto;
	}
</style>
