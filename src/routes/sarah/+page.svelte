<script>
	import { livros } from '$lib/sarah.js';

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
                            bind:value={busca}
                            oninput={filtrar}
						/>
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
				<img src="favicon.png" class="img-fluid rounded-start" alt="..." />
			</div>
			<div class="col-md-8">
				<div class="card-body">
					<h5 class="card-title"><b>Sarah Adams</b></h5>
                    <h7 class="card-title"><b>@authorsarahadams</b></h7>
                    <br>
                    <br>
					<p class="card-text">
						Nascida e criada em Nashville TN, Sarah Adams ama sua família, dias quentes e fazer as pessoas sorrirem.
                        <p>Sarah sonha em ser escritora desde menina, mas finalmente escreveu seu primeiro romance quando suas filhas estavam cochilando e ela não tinha mais desculpas para adiar.
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
    {#each filtrados as livro }
        
	<div class="col d-flex align-items-center">
		<div class="border p-2">
			<img style="width:200px" src="{livro.imagem}" alt="..." />
    </div>
	</div>
    {/each}
	
</div>

<p>sarah</p>

<style>
	.haipados {
		text-align: center;
		color: rgb(137, 40, 228);
	}
</style>
