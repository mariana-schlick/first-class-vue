<template>
    <div class="componente">
        <h1>Componente com dados</h1>
        <p>Nome: {{ nomeProduto }} - {{ codigoProduto }}</p>
    </div>
</template>

<script setup> // Com script setup não precisamos usar return
const nomeProduto= "Apontador"
const codigoProduto = "#987"
</script>