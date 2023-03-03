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
</script>

<template>
   <button @click="incrementarContador">+</button>
  <button @click="decrementarContador">-</button>
  <button @click="Reiniciar">C</button>
  <p>Valor do contador é: {{ contador }}</p>
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
  background-color: #af4c86;
  border: none;
  border-radius: 15px;
  box-shadow: 0 9px #999;
}


</style>
