<template>
    <div class="componente">
        <h1>Componente com dados Reativos Não Primitivos</h1>
        <p>Nome: {{ pessoa.nome }} | Idade: {{ pessoa.idade }}</p>
        <button @click="fazerAniversario()">Fazer Aniversário</button>
        <button @click="mudarNome()">Mudar nome</button> 
    </div>
</template>


<!-- <script setup>

    import {reactive} from "vue"

    const pessoa = reactive({nome:"Ana",idade: 27})

    function fazerAniversario(){
        pessoa.idade += 1
    }

    function mudarNome(){
        pessoa.nome = "Ana Maria"
    }

</script> -->



<!-- Usando opetions API -->
<script>
export default{
    data: function(){
        return{
            pessoa:{
                nome:"Ana",
                idade:27
            }
        }
    },
    methods:{
        fazerAniversario: function(){
            this.pessoa.idade += 1
        },
        mudarNome: function(){
            this.pessoa.nome = "Ana Maria"
        }
    }

}

</script>