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
  <span class="titulo">
    <h1 style="color: rgb(255, 255, 255);">Black List</h1>
    <h1 style=" color: rgb(255, 255, 255);">Total: {{ formatarPreco(carrinho.total) }} </h1>
  </span>
  </div>
  <div class="container-geral">
    <listagem-livros/>
    <carrinho-principal/>
  </div>
</template>

<style scoped>
.container-geral {
  /* display: flex;
  justify-content: space-between; */
  display: grid;
  grid-template-columns: 3fr 1fr;
}

.titulo {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}

</style>
