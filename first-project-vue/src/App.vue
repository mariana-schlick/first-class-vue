<script setup>
import PrimeiroComponente from "./components/PirmeiroComponente.vue"
import ComDados from "./components/ComDados.vue"
import ComDadosReativosPrimitivos from "./components/ComDadosReativosPrimitivos.vue";
import ComDadosReativosNaoPrimitivos from "./components/ComDadosReativosNaoPrimitivos.vue";
import DataBinding from "./components/DataBinding.vue";
import ComProps from "./components/ComProps.vue";
import EscutaEvento from "./components/EscutaEvento.vue";
</script>

<template>
  <header>Vue</header>
  <PrimeiroComponente/>
  <ComDados/>
  <ComDadosReativosPrimitivos/>
  <ComDadosReativosNaoPrimitivos/>
  <DataBinding/>
  <ComProps item="Borracha" :preco="2.50"/> <!-- Comunicação entre componente PAI com componente FILHO -->
  <EscutaEvento/>
</template>
