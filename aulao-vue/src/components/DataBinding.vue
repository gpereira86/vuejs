<template>
    <div class="componente">
        <h1>Componente com Data Binding</h1>
        <p>{{ valor }}</p>
        <!-- <input type="text" v-bind:value="valor"></input> --> <!-- one way data binding, apenas uma direçao de dados -->
        <!--<input type="text"
            v-bind:value="valor"
            v-on:input="(e)=>valor = e.target.value">
        </input>--> <!-- two way data binding, duas direções de dados -->

            <!-- Atalhos:
             v-bind usar apenas ':' exemplo :value 
             v-on usar apenas '@' exemplo: @input-->

        <input type="text" v-model="valor"></input> <!-- outra forma two way data binding, mais comum -->

    </div>
</template>

<script setup>
import {ref} from "vue"
const valor = ref("Vue é muito legal --->")
</script>