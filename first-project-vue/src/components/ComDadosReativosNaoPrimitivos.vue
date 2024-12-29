<template>
    <div class="componente">
        <h1>Componente Com Dados Reativos Não Primitivos</h1>
        <p>Nome: {{ pessoa.nome }} | Idade: {{ pessoa.idade }}</p>

        <!-- Para chamar as funções, devemos editar os buttons da forma abaixo,
        caso formos passar parâmetros, usar os (), caso não, não usar, o v-on
        pode ser substituido por @ -->
        <button @click="fazerAniversario">Fazer aniversário</button>
        <button @click="mudarNome()">Mudar nome</button>
    </div>
</template>

<script setup>
import {reactive} from "vue"

const pessoa = reactive({nome: "Mariana", idade:30})

function mudarNome(){
    pessoa.nome = "Ana"
}

function fazerAniversario(){
    pessoa.idade +=1
}

</script>