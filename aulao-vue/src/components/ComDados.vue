<template>
    <div>
        <h1>Componente com dados</h1>
        <p>Nome: caneta - #123</p>
    </div>
</template>

<style scoped>
    div{
        text-align: center;
        border: 2px solid rgb(10, 69, 4);
        background-color: #050d04;
        border-radius: 15px;
        margin: 30px;
        padding: 10px;
    }
</style>

<script>
// options API -> sempre usar function, nunca arrow
export default{
    data: function(){
        return{}
    }
}
</script>