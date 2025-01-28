<script>
  import CartaMagic from '$lib/components/CartaMagic.svelte';
  import { cards } from '$lib/data.js';
  import { goto } from '$app/navigation'

</script>
<div class="botões">
<button onclick={goto('/sobre')} class="rounded-circle"><img src="favicon.png" width="200px" class="rounded-circle"></button> oiiii
<button onclick={goto('/sobre')} class="rounded-circle"><img src="favicon.png" width="200px" class="rounded-circle"></button> oiiii
<button onclick={goto('/sobre')} class="rounded-circle"><img src="favicon.png" width="200px" class="rounded-circle"></button> oiiii
<button onclick={goto('/sobre')} class="rounded-circle"><img src="favicon.png" width="200px" class="rounded-circle"></button> 
</div>
 
<div class="row g-4">
  {#each cards as card}
    <div class="col">
      <CartaMagic {...card} />
    </div>
  {/each}
</div>

<h1>oii</h1>
<p>aaa</p>
<a href="/sobre">sobre</a>

<style>
  .botões {
text-align: center;
color: aliceblue;
  }
</style>



