<script setup>



import CarrinhoPrincipal from '@/components/CarrinhoPrincipal.vue'
import ListagemLivros from '@/components/ListagemLivros.vue'




</script>

<template>
  <div>
    <h1 style="color: rgb(255, 255, 255);">Minha livraria</h1>
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

.carrinho {
  /* min-width: 20%; */
}

</style>
