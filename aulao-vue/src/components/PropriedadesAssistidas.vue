<template>
    <div class="componente">
        <h1>Componente com Propriedades Assistidas</h1>
        <p>Idade: {{ idade }}</p>
        
        <label>Ano Nascimento:</label>
        <input type="number" v-model="anoNascimento" min="1900"> <br>
        
        <label>Ano Atual:</label>
        <input type="number" v-model="anoAtual" min="2000">
    </div>
</template>

<!-- <script setup>
import {ref, watch} from "vue"

const anoNascimento = ref(1900)
const anoAtual = ref(2000)

const idade = ref(0)

watch(anoAtual, (ano)=>{
    idade.value = ano - anoNascimento.value
})

watch(anoNascimento, (ano)=>{
    idade.value = anoAtual.value - ano
})
</script> -->


<!-- Outra forma de fazer o o mesmo -->
<script setup>
import {ref, watchEffect} from "vue"

const anoNascimento = ref(1900)
const anoAtual = ref(2000)
const idade = ref(0)

watchEffect(()=>{
    idade.value = anoAtual.value - anoNascimento.value
})

</script>


<style scoped>
label{
    margin: 10px;
}
</style>