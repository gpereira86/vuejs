<template>
    <div class="componente">
        <h1>Componente com dados Reativos Primnitivos</h1>
        <p>Nome: {{ nome }} | Idade: {{ idade }}</p>
        <button v-on:click="fazerAniversario()">Fazer Aniversário</button>
        <button @click="mudarNome()">Mudar nome</button>  <!-- usar @ é o mesmo que usar v-on -->
    </div>
</template>

<script setup>

import {ref} from "vue" // Vue permite alterar o valor das variáveis

    const nome = ref("Ana")
    const idade = ref(27)

    function fazerAniversario(){
        idade.value += 1
    }

    function mudarNome(){
        nome.value = "Ana Maria"
    }
</script>