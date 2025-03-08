<template>
    <div class="componente">
        <h1>Componente que Escuta Evento</h1>
        <p>Total: R$ {{ total }}</p>

        <div class="lista">
            <EmiteEvento item="item1" :preco="1.99" @foiAdicionado="atualizarTotal"/>
            <EmiteEvento item="item2" :preco="5.00" @foiAdicionado="atualizarTotal"/>
            <EmiteEvento item="item3" :preco="10.99" @foiAdicionado="atualizarTotal"/>
        </div>

    </div>
</template>

<script setup>
import { ref } from 'vue';
import EmiteEvento from './EmiteEvento.vue';

const total = ref(0)

function atualizarTotal(p) {
    const valor = total.value + p
    total.value = +valor.toFixed(2)
}
</script>

<style scoped>
.lista{
    display: flex;
    justify-content: space-between;
    font-size: 0.7rem;
}
</style>