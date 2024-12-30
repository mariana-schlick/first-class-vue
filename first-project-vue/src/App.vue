<script setup>
import PrimeiroComponente from "./components/PrimeiroComponente.vue"
import ComDados from "./components/ComDados.vue"
import ComDadosReativosPrimitivos from "./components/ComDadosReativosPrimitivos.vue";
import ComDadosReativosNaoPrimitivos from "./components/ComDadosReativosNaoPrimitivos.vue";
import DataBinding from "./components/DataBinding.vue";
import ComProps from "./components/ComProps.vue";
import EscutaEvento from "./components/EscutaEvento.vue";
import PropriedadesComputadas from "./components/PropriedadesComputadas.vue"
import PropriedadesAssistidas from "./components/PropriedadesAssistidas.vue";
import RenderizacaoCondicional from "./components/RenderizacaoCondicional.vue";
import RenderizacaoListas from "./components/RenderizacaoListas.vue";
import Slots from "./components/Slots.vue";

const borracha = "borracha"
const precoBorracha = 2.50

const cachorrosDoJoao = [
  {nome: "Totó", idade:2},
  {nome: "Bento", idade:5},
  {nome: "Naninha", idade:11}
]

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
  <PropriedadesComputadas/>
  <PropriedadesAssistidas/>
  <RenderizacaoCondicional nome="Mariana" :qtde-cachorros="2"/>
  <RenderizacaoListas nome="João" :cachorros="cachorrosDoJoao"/>
  <Slots>
    <template v-slot:icone>
      <svg  xmlns="http://www.w3.org/2000/svg"  width="24"  height="24"  viewBox="0 0 24 24"  fill="none"  stroke="currentColor"  stroke-width="2"  stroke-linecap="round"  stroke-linejoin="round"  class="icon icon-tabler icons-tabler-outline icon-tabler-alert-square-rounded">
        <path stroke="none" d="M0 0h24v24H0z" fill="none"/>
        <path d="M12 3c7.2 0 9 1.8 9 9s-1.8 9 -9 9s-9 -1.8 -9 -9s1.8 -9 9 -9z" />
        <path d="M12 8v4" />
        <path d="M12 16h.01" />
      </svg>
    </template>
  </Slots>
</template>
