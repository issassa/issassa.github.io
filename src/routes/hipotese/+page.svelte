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
	<nav class="navbar" style="background-color: #118aa5;">
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
					src="hipotese.png"
					class="img-fluid rounded-start"
					alt="..."
					width="600px"
					height="990px"
				/>
			</div>
			<div class="col-md-6">
				<div class="card-body">
					<h4 class="card-title"><b>A Hipótese Do Amor</b></h4>
					<br />
					<h7 class="card-title"><b>Autora: Ali Hazelwood</b></h7>
					<p><h7 class="card-title"><b>@alihazelwood</b></h7></p>
					<br />
					<p class="card-text">
						A história começa com um prólogo surpreendente, com um encontro inusitado de Adam
						Carlsen e Olive Smith. Mesmo não sabendo quem são, o encontro deles é cheio de trocas de
						ideais e motivações para o futuro. Adam, é professor e cientista com grandes teses
						publicadas, já Olive é uma estudante de doutorado, que quer provar que com um tratamento
						diferenciado, poderá alcançar o diagnóstico do câncer mais cedo. Os dois não sabiam, mas
						dois anos e onze meses depois, esse encontro iria acontecer novamente.
					</p>
					<a
						href="https://www.amazon.com.br/hip%C3%B3tese-amor-Sucesso-TikTok/dp/6555653302/ref=sr_1_1?crid=3IWI0K6LX87AM&dib=eyJ2IjoiMSJ9.5TvQRwu_yW7b07AzYz3mXiyhgG3KAsZ2USozdUog9u2F5H5UDiCToflQ1T3kibB-CCUQbzvZVLwarzH-7PRQ5VXS3sZq_pKrEufAPTL04vYoyZ00UXcudmKPfOoHczj6PaUjnRlvlZbb0_g2Rx4_d-jTKPu7tARdel0mxzC1ZtqpCQLXRgq4bgaYSG_MLZxwVNLKLlDhsdYRa-UuiECssK1oNTZVCcIaqJeP6bHCLNYwpBuxzWLH-GlKf2iY-hveDninTLBa01WrnnDhqrPib-BrwvMArC8OvaKsP3YRRDbJ3JK5W4XQ8ttKztpkkyoLN_BH8YBm01QWJ59VpWvS8-jZxPAKC6_0E3FAPHVpMQxd2qWtTVP0Ypdf300-BZ1jrk99QkGU_xbW7U__oHpIkE4uudMtQ5MV1Mq4o5vdw-7PVVsP6UjoMNquj8LoDAEF.EJcSkZNvd-oEfl_Q4O8j3yEFdKWQlgWKaUjpDO2jJtY&dib_tag=se&keywords=a+hipotese+do+amor&qid=1739282869&sprefix=a+hipo%2Caps%2C330&sr=8-1&ufe=app_do%3Aamzn1.fos.6d798eae-cadf-45de-946a-f477d47705b9"
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
			background-color: #118aa5;
		}
	</style>
</svelte:head>
