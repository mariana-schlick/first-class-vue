<template>
    <div class="componente">
        <h1>Componente Com Dados Reativos Primitivos</h1>
        <p>Nome: {{ nome }} | Idade: {{ idade }}</p>

        <!-- Para chamar as funções, devemos editar os buttons da forma abaixo,
        caso formos passar parâmetros, usar os (), caso não, não usar, o v-on
        pode ser substituido por @ -->
        <button v-on:click="fazerAniversario">Fazer aniversário</button>
        <button @click="mudarNome()">Mudar nome</button>
    </div>
</template>

<script setup>
// Para o vue 'saber' que pode ser alterado o valor das constantes, devemos
// importar
import {ref} from "vue"
    // Para que a constante seja alterada, incluir o ref
    const nome = ref("Mariana")
    const idade = ref(27)

    // Para alterar os valores, devemos usar a sintaxe abaixo
    function fazerAniversario(){
        idade.value +=1
    }

    function mudarNome (){
        nome.value = "Ana"
    }
</script>