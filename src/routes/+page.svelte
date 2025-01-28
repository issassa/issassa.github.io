<script>
  import CartaMagic from '$lib/components/CartaMagic.svelte';
  import { cards } from '$lib/data.js';
  import { goto } from '$app/navigation';
</script>



<nav class="navbar bg-dark border-bottom border-body" data-bs-theme="dark">
  <div class="container-fluid">
    <a class="navbar-brand" href=".">
      <img src="/docs/5.3/assets/brand/bootstrap-logo.svg" alt="" width="30" height="24" class="d-inline-block align-text-top">
      <b>BiblioBella</b>
    </a>
  </div>
  </nav>
  <div class="card text-bg-dark">
    <img src="..." class="card-img" alt="...">
    <div class="card-img-overlay">
      <h5 class="card-title">Card title</h5>
      <p class="card-text">This is a wider card with supporting text below as a natural lead-in to additional content. This content is a little bit longer.</p>
      <p class="card-text"><small>Last updated 3 mins ago</small></p>
    </div>
  </div>
<br>
<br>
<div class="autorpreferido">
  <h2><b>Meus autores favoritos</b></h2>
  </div>
<br>
<br>

<div class="botões">
<button onclick={goto('/lynn')} class="rounded-circle"><img src="favicon.png" width="200px" class="rounded-circle"></button> oiiii
<button onclick={goto('/ali')} class="rounded-circle"><img src="favicon.png" width="200px" class="rounded-circle"></button> oiiii
<button onclick={goto('/sarah')} class="rounded-circle"><img src="favicon.png" width="200px" class="rounded-circle"></button> oiiii
<button onclick={goto('/emily')} class="rounded-circle"><img src="favicon.png" width="200px" class="rounded-circle"></button> 
</div>

<br>
<br>
<br>
<div class="livropreferido">
<h2><b>Meus livrinhos favoritos</b></h2>
</div>
<br>
<br>
<div class="row row-cols-1 row-cols-md-3 g-4">
  <div class="col">
    <div class="card">
      <img src="..." class="card-img-top" alt="...">
    </div>
  </div>
  <div class="col">
    <div class="card">
      <img src="..." class="card-img-top" alt="...">
    </div>
  </div>
  <div class="col">
    <div class="card">
      <img src="..." class="card-img-top" alt="...">
    </div>
  </div>
  <div class="col">
    <div class="card">
      <img src="..." class="card-img-top" alt="...">
    </div>
  </div>
  <div class="col">
    <div class="card">
      <img src="..." class="card-img-top" alt="...">
    </div>
  </div>
  <div class="col">
    <div class="card">
      <img src="..." class="card-img-top" alt="...">
    </div>
  </div>
  <div class="col">
    <div class="card">
      <img src="..." class="card-img-top" alt="...">
    </div>
  </div>
  <div class="col">
    <div class="card">
      <img src="..." class="card-img-top" alt="...">
    </div>
  </div>
  <div class="col">
    <div class="card">
      <img src="..." class="card-img-top" alt="...">
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
  .livropreferido{
    text-align: center;
    color:rgb(137, 40, 228)
  }
  .autorpreferido{
    text-align: center;
    color:rgb(137, 40, 228)
  }
</style>





