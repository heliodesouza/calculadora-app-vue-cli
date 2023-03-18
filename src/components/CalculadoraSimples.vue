<template>
  <div class="calculadora">
    <div class="display">{{valorCorrente || '0'}}</div>
    <div v-on:click="limpar" class="botao">C</div>
    <div v-on:click="sinal" class="botao">+/-</div>
    <div v-on:click="porcentagem" class="botao">%</div>
    <div v-on:click="dividir" class="botao operadores">÷</div>
    <div v-on:click="juntarNumeros('7')" class="botao">7</div>
    <div v-on:click="juntarNumeros('8')" class="botao">8</div>
    <div v-on:click="juntarNumeros('9')" class="botao">9</div>
    <div v-on:click="multiplicar" class="botao operadores">x</div>
    <div v-on:click="juntarNumeros('4')" class="botao">4</div>
    <div v-on:click="juntarNumeros('5')" class="botao">5</div>
    <div v-on:click="juntarNumeros('6')" class="botao">6</div>
    <div v-on:click="diminuir" class="botao operadores">-</div>
    <div v-on:click="juntarNumeros('1')" class="botao">1</div>
    <div v-on:click="juntarNumeros('2')" class="botao">2</div>
    <div v-on:click="juntarNumeros('3')" class="botao">3</div>
    <div v-on:click="somar" class="botao operadores">+</div>
    <div v-on:click="juntarNumeros('0')" class="botao zero">0</div>
    <div v-on:click="ponto" class="botao">.</div>
    <div v-on:click="resultado" class="botao operadores">=</div>
  </div>
</template>

<script src="./Calculadora.js"></script>

<style>
.calculadora {
   height: 320px;
    width: 235px;
    border-radius: 5px;
    overflow: hidden;
    display: grid;
    grid-template-columns: repeat(4, 25%);
    grid-template-rows: 1fr 48px 48px 48px 48px 48px;
}
.display {
   grid-column: span 4;
        background-color: #0004;
        display: flex;
        justify-content: flex-end;
        align-items: center;
        padding: 20px;
        font-size: 2.1em;
        overflow: hidden;
        color: white;
}
.zero {
  grid-column: 1 / 3;
}
.botao {
  cursor: pointer;
  font-size: 1.4em;
  background-color: #f2f2f2;
  color:black;
  border: none;
  border: 1px solid #999;
  outline: none;
}
.operadores {
  background-color: rgb(55, 156, 80);
  color: white;
}

</style>
