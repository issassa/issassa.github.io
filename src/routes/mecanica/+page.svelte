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

<div class="barra">
	<nav class="navbar" style="background-color: #d45d5a;">
		<div class="container-fluid">
			<a class="navbar-brand" href=".">
				<img src="book.svg" alt="." width="30" height="24" class="d-inline-block align-text-top" />
				<b>BlogBook</b>
			</a>
			<nav class="navbar navbar-expand-lg">
				<div class="container-fluid">
					<div class="collapse navbar-collapse" id="navbarTogglerDemo02"></div>
				</div>
			</nav>
		</div>
	</nav>
</div>
<br />
<br />
<div class=" d-flex justify-content-center">
	<div class="card mb-3" style="max-width: 800px;">
		<div class="row g-0">
			<div class="col-md-6">
				<img
					src="mecanica.png"
					class="img-fluid rounded-start"
					alt="..."
					width="600px"
					height="990px"
				/>
			</div>
			<div class="col-md-6">
				<div class="card-body">
					<h4 class="card-title"><b>A Mecânica Do Amor</b></h4>
					<br />
					<h7 class="card-title"><b>Autora: Alexene Farol Follmuth</b></h7>
					<p><h7 class="card-title"><b>@afarolfollmuth</b></h7></p>
					<br />
					<p class="card-text">
						Bel não sabe o que fazer quando se formar no colégio e nem quer pensar no assunto. Mas
						quando revela um talento especial para engenharia, é incentivada por uma professora a
						entrar para o clube de robótica da escola. O problema é que o clube é comandado por Teo,
						que além de gato e popular, ainda é mega inteligente e já tem cada passo do seu
						brilhante futuro bem planejado. Quando os dois se conhecem, o choque é instantâneo: eles
						se odeiam. Mas conforme trabalham juntos em robôs de combate, Teo logo reconhece o
						talento de Bel e percebe que não consegue parar de pensar na constelação de sardas no
						rosto da garota. E, pior ainda, se vê dedicado a aprender a discografia de Taylor Swift,
						de quem ela é fã.
					</p>
					<a
						href="https://www.amazon.com.br/mec%C3%A2nica-amor-Alexene-Farol-Follmuth/dp/6588131992/ref=sr_1_1?adgrpid=1144592599016327&dib=eyJ2IjoiMSJ9.oeAqljkec3A-XI4Rvpi7x7QNwaewY8LBt-p9SGakW5MNxEkFWtM9NAmr30jSrAgykBUZgJnht8z-l3C0T7SRxORIarBkXQTY7UFVbtNyr4I3SkMfcTrw7Hq8NUVkeifnLcE3ruFGj4clYljCw6RE54-sbkI-qqjz5Fq5yCqI7mucxw_cDhHEXq2Gy-Gw-ah9GnYWCrlYNxsUHUur7meWuFfr07i9VI5cgWUbySqNaOtqwtFJWW_iEulW2eJTyQAG7hQZjRg9eJFWymwAQAL3ucKRZF94wPKqrMVzO6YqgxWg4IkTR88rmHZX_Ank65UevZa8QVELKVpLECOzb3kFBYvMJ2VMB49B0o_kPOxuO6JQ-O6voMKoCqCTryXjehCqaIGSG8oxNmKSaoBU9xPqJk77yFJwpkjrONHW4YXdOl7q-YqDof8XoSfQ2V-BNFYP.2PjPYfjNKRFD2g4o7oiEaizB4JvuEvFjIWK2mIz_11E&dib_tag=se&hvadid=71537206328805&hvbmt=be&hvdev=c&hvlocphy=185107&hvnetw=o&hvqmt=e&hvtargid=kwd-71537739873060%3Aloc-20&hydadcr=19176_13421861&keywords=a+mec%C3%A2nica+do+amor&qid=1739281765&sr=8-1"
						>compre aqui</a
					>
				</div>
			</div>
		</div>
	</div>
</div>
<br />
<br />

<svelte:head>
	<style>
		body {
			background-color: #d45d5a;
		}
	</style>
</svelte:head>
