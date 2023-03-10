<script setup>


import { ref, onMounted } from 'vue'

let contador = ref(0)


function incrementarContador() {
  contador.value++
}
function decrementarContador() {
  if (contador.value > 0)
   {contador.value-- }
  
  
}
function Reiniciar() {
    contador.value = 0
  }

onMounted(() => {
  console.log(`O valor inicial do contador é ${contador.value}.`)
})
  const rawHtml = '<span style="color: red">Este é um texto em vermelho</span>'
  const numero = 1
    const ok = true
    const mensagem = 'programar'
    function inverter(mensagem) {
        return mensagem.split('').reverse().join('')
    }

    const url = 'https://vuejs.org/'
    
   
    
</script>

<template>
   <button @click="incrementarContador">+</button>
  <button @click="decrementarContador">-</button>
  <button @click="Reiniciar">C</button>
  <p>Valor do contador é: {{ contador }}</p>
   <p>Usando interpolação de textos: {{rawHtml}}</p>
    <p>Usando v-html: <span v-html="rawHtml"></span></p>
  <span>Valor do contador: {{ contador }}</span>

 <p> {{ numero + 1 }}</p>
<p>{{ ok ? 'Sim' : 'Não' }}</p>
<p>{{ mensagem.split('').reverse().join('') }}</p>
<p>{{ inverter(mensagem) }}</p>

<div v-if="ok">Mostrar</div>

<button v-on:click="algumaFuncao"> <a v-bind:href="url">Mais informações...</a> </button>
<form v-on:submit.prevent="algumaFuncao"> the end... </form>


</template>


<style scoped>



button {
  font-weight: bold;}
  button {
  display: inline-block;
  padding: 15px 25px;
  font-size: 24px;
  margin: 20px;
  cursor: pointer;
  text-align: center;
  text-decoration: none;
  outline: none;
  color: #fff;
  background-color: #634caf;
  border: none;
  border-radius: 15px;
  box-shadow: 0 9px #999;
}
a{
color: #fff;
}


</style>
