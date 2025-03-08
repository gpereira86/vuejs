<script setup>
import PrimeiroComponente from "./components/PrimeiroComponente.vue"
import ComDados from "./components/ComDados.vue"
import ComDadosReativosPrimitivos from "./components/ComDadosReativosPrimitivos.vue";
import ComDadosReativosNaoPrimitivos from "./components/ComDadosReativosNaoPrimitivos.vue";
import DataBinding from "./components/DataBinding.vue";
import ComProps from "./components/ComProps.vue";
import EscutaEvento from "./components/EscutaEvento.vue";
import PropriedadesComputadas from "./components/PropriedadesComputadas.vue";
import PropriedadesAssistidas from "./components/PropriedadesAssistidas.vue";

const borracha = "Borracha"
const precoBorracha = 2.50
</script>

<template>
  <header>Vue</header>
  <PropriedadesAssistidas/>
  <PropriedadesComputadas/>
  <EscutaEvento/>
  <ComProps v-bind:item="borracha" v-bind:preco="precoBorracha"/>
  <DataBinding/>
  <ComDadosReativosNaoPrimitivos/>
  <ComDadosReativosPrimitivos/>
  <ComDados/>
  <PrimeiroComponente/>
</template>


