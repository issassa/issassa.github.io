<script>
	import CartaMagic from '$lib/components/CartaMagic.svelte';
	import { cards } from '$lib/data.js';
	import { goto } from '$app/navigation';
</script>

<div class="barra">
	<nav class="navbar bg-body-tertiary">
		<div class="container-fluid">
			<a class="navbar-brand" href=".">
				<img src="book.svg" alt="." width="30" height="24" class="d-inline-block align-text-top" />
				<b>BlogBook</b>
			</a>
		</div>
	</nav>
</div>
<div class="mb-3">
  <img src="blog.png" class="" alt="..." style="max-width: 90%; max-height: 90%;">
</div>
<div class="autorpreferido">
	<h2><b>Autores favoritos</b></h2>
</div>
<br />
<br />

<div class="botões">
	<a href="/lynn" class="rounded-circle"
		><img src="lynn.png" width="200px" height="200px" class="rounded-circle" /></a
	>
	oiiii
	<a href="/ali" class="rounded-circle"
		><img src="ali.png" width="200px" height="200px" class="rounded-circle" /></a
	>
	oiiii
	<a href="/sarah" class="rounded-circle"
		><img src="sarah.png" width="200px" height="200px" class="rounded-circle" /></a
	>
	oiiii
	<a href="/emily" class="rounded-circle"
		><img src="emily.png" width="200px" height="200px" class="rounded-circle" /></a
	>
</div>

<br />
<br />
<br />
<div class="livropreferido">
	<h2><b>Livrinhos favoritos</b></h2>
</div>
<br />
<br />
<div class="cardsinicio">
	<div class="row row-cols-3 row-cols-md-4 g-4">
		<div class="col">
			<div class="card">
				<a href="/lynn"><img src="emily.png" class="card-img-top" alt="mecanica" /></a>
			</div>
		</div>
		<div class="col">
			<div class="card">
				<img src="melhor.png" class="card-img-top" alt="..." />
			</div>
		</div>
		<div class="col">
			<div class="card">
				<img src="nãoé.png" class="card-img-top" alt="..." />
			</div>
		</div>
		<div class="col">
			<div class="card">
				<img src="hipotese.png" class="card-img-top" alt="..." />
			</div>
		</div>
		<div class="col">
			<div class="card">
				<img src="amor por.png" class="card-img-top" alt="..." />
			</div>
		</div>
		<div class="col">
			<div class="card">
				<img src="teoricamente.png" class="card-img-top" alt="..." />
			</div>
		</div>
		<div class="col">
			<div class="card">
				<img src="eue.png" class="card-img-top" alt="..." />
			</div>
		</div>
		<div class="col">
			<div class="card">
				<img src="amorroma.png" class="card-img-top" alt="..." />
			</div>
		</div>
		<div class="col">
			<div class="card">
				<img src="apostando.png" class="card-img-top" alt="..." />
			</div>
		</div>
	</div>
</div>

<p>aaa</p>
<a href="/sobre">sobre</a>

<style>
	.botões {
		text-align: center;
		color: rgb(255, 255, 255);
	}
	.livropreferido {
		text-align: center;
		color: #000000;
		font-family: cursive;
	}
	.autorpreferido {
		text-align: center;
		color: rgb(0, 0, 0);
		font-family: cursive;
	}
	.cardsinicio {
		text-align: center;
		width: 500px;
		height: 500px;
	}
	.barra {
		color: #000000;
	}
	.nome {
		color: rgb(255, 255, 255);
	}
</style>
