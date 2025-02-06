<script>
	import { livros } from '$lib/ali.js';

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
	<div class="card mb-3" style="max-width: 850px;">
		<div class="row g-0">
			<div class="col-md-6">
				<img src="ali.png" class="img-fluid rounded-start" alt="..." />
			</div>
			<div class="col-md-6">
				<div class="card-body">
					<h5 class="card-title"><b>Ali Hazelwood</b></h5>
                    <h7 class="card-title"><b>@alihazelwood</b></h7>
                    <br>
                    <br>
					<p class="card-text">
						Ali Hazelwood é uma escritora e neurocientista italiana que tem vindo a conquistar um lugar de destaque no que à ficção romântica diz respeito.
                        Cresceu na Itália e viveu no Japão e na Alemanha antes de se estabilizar nos Estados Unidos para se doutorar em Neurociência.
						<p>Autora de diveros livros famosos como "A Hipótese do Amor", "A Razão do Amor", "A Teoria do Amor", entre outros fenômenos de ficção romântica.
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

<p>ali</p>

<style>
	.haipados {
		text-align: center;
		color: rgb(0, 0, 0);
	}
</style>
