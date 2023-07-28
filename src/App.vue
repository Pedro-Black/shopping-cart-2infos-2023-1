<script setup>
import {carrinho} from '@/_data/carrinho.js'
function formatarPreco(preco) {
  return 'R$ ' + preco.toFixed(2).replace('.', ',')
}


import CarrinhoPrincipal from '@/components/CarrinhoPrincipal.vue'
import ListagemLivros from '@/components/ListagemLivros.vue'




</script>

<template>
<div class="cabeçario">
  <div class="titulo">
    <h1>
      <span class="branco">Black</span>
      <span class="laranja ml-5">List</span>
    </h1>
    <h1>
      <span class="branco">Total: {{ formatarPreco(carrinho.total) }}</span>
    </h1>
  </div>
  </div>
  <div class="container-geral">
    <listagem-livros/>
    <carrinho-principal/>
  </div>
</template>

<style scoped>
.container-geral {
  display: grid;
  grid-template-columns: 3fr 1fr;
}

.titulo {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  padding: 0 20px 0 10px;
  font-size: 1.5rem;
}
.branco {
  color: rgb(255, 255, 255);
}

.laranja {
  color:rgb(210, 105, 30)
}

.ml-5{
  margin-left: .5em;
}

</style>
