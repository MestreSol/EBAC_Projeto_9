<script setup lang="ts">
import { ref } from 'vue';
import LCD from './LCD.vue'; // Importando o componente LCD

let conta = ref(''); // Variável reativa para a conta

const lcdDisplay = ref([]); // Variável reativa para o LCD como uma lista de textos

function seven() {
    conta.value += '7';
    lcdDisplay.value.push('7');
}

function eight() {
    conta.value += '8';
    lcdDisplay.value.push('8');
}

function nine() {
    conta.value += '9';
    lcdDisplay.value.push('9');
}

function four() {
    conta.value += '4';
    lcdDisplay.value.push('4');
}

function five() {
    conta.value += '5';
    lcdDisplay.value.push('5');
}

function six() {
    conta.value += '6';
    lcdDisplay.value.push('6');
}

function one() {
    conta.value += '1';
    lcdDisplay.value.push('1');
}

function two() {
    conta.value += '2';
    lcdDisplay.value.push('2');
}

function three() {
    conta.value += '3';
    lcdDisplay.value.push('3');
}

function zero() {
    conta.value += '0';
    lcdDisplay.value.push('0');
}

function dot() {
    conta.value += '.';
    lcdDisplay.value.push('.');
}


function sum() {
    conta.value += '+';
    lcdDisplay.value.push('+');
}

function sub() {
    conta.value += '-';
    lcdDisplay.value.push('-');
}

function mult() {
    conta.value += '*';
    lcdDisplay.value.push('*');
}

function div() {
    conta.value += '/';
    lcdDisplay.value.push('/');
}

function del() {
    conta.value = conta.value.slice(0, -1);
    lcdDisplay.value.pop();
}

function AC() {
    conta.value = '';
    lcdDisplay.value = [];
}

function equal() {
    conta.value = eval(conta.value);
    lcdDisplay.value = [conta.value];
}

</script>

<template>
    <div class="tela">
        <LCD :display="lcdDisplay" /> 
    </div>
    <div class="row numeric">
        <button @click="seven">7</button>
        <button @click="eight">8</button>
        <button @click="nine">9</button>
        <button @click="del">DEL</button>
        <button @click="AC">AC</button>
    </div>
    <div class="row numeric">
        <button @click="four">4</button>
        <button @click="five">5</button>
        <button @click="six">6</button>
        <button @click="mult">x</button>
        <button @click="div">/</button>
        </div> 
        <div class="row numeric">
        <button @click="one">1</button>
        <button @click="two">2</button>
        <button @click="three">3</button>
        <button @click="sum">+</button>
        <button @click="sub">-</button>
        </div>
        <div class="row numeric">
        <button @click="zero">0</button>
        <button @click="dot">.</button>
        <button @click="equal">=</button>
        </div>
</template>

<style lang="css">
.lcd{
    display:none;
}

.enable{
    display: flex;
    justify-content: center;
}
    .row{
        display: flex;
        justify-content: space-between;
        margin-top: 10px;
    }
    .function button{
        width: 50px;
        height: 50px;
        border-radius: 50%;
        background-color: #f2f2f2;
        border: 1px solid #ccc;
        font-size: 20px;
        font-size: small;
    }
    .function button:hover{
        background-color: #ccc;
    }
    .function button:active{
        background-color: #999;
    }
    .function button:focus{
        outline: none;
    }
    .tela{
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: #f2f2f2;
  border: 1px solid #ccc;
  border-radius: 10px;
  width: 250px;
  height: 100px;
  margin: 0 auto;
  top:0px;
  
}
    .operation button{
        width: 50px;
        height: 25px;
        background-color: #000;
        border: 1px solid #000;
        font-size: 20px;
        font-size: small;
        color: #fff;
    }

    .operation button:hover{
        background-color: #333;
    }

    .operation button:active{
        background-color: #666;
    }

    .operation button:focus{
        outline: none;
    }

    .numeric button{
        width: 50px;
        height: 50px;
        background-color: #f2f2f2;
        border: 1px solid #ccc;
        font-size: 20px;
        font-size: small;
    }

    .numeric button:hover{
        background-color: #ccc;
    }

    .numeric button:active{
        background-color: #999;
    }

    .numeric button:focus{
        outline: none;
    }

    .numeric button:active{
        background-color: #999;
    }

    
.display-tools {
    display: flex;
    justify-content: space-between;
    width: 100%;
    padding: 0 10px;
    margin-bottom: 10px;
    align-items: center;
}

.display-tools li {
    list-style: none;
    color: white;
    cursor: pointer;
}

.display-tools li.active {
    color: black;
}

</style>
