<template>
    <div>
        <input class="input" type="number" v-model.number="operand1" placeholder="первое число"/>
        <input class="input" type="number" 
            v-model.number="operand2" 
            placeholder="второе число" 
        />
         <b> = </b> <h3> {{ sum }} </h3>

        <div class="keyboard">
            <button class="operation" @click="sum = operand1 + operand2">+</button>
            <button class="operation" @click="sum = operand1 - operand2">-</button>
            <button class="operation" @click="mult">*</button>
            <button class="operation" @click="div">/</button>
            <button class="operation" @click="pow">^</button>
            <button class="operation" @click="floor">//</button>

        </div>
    </div>
</template>

<script>
export default {
    name: "Calculator",
    data(){
        return {
            text: "Some string",
            operand1: null,
            operand2: null,
            sum: 0
        }
    },
    methods: {
        mult() {
            this.sum = this.operand1 * this.operand2
        },
        div() {
            this.sum = this.operand1 / this.operand2
        },
        pow(){
            this.sum = this.operand1 ** this.operand2
        },
        floor(){
            this.sum = this.operand1 % this.operand2
        }
    },
}
</script>

<style>
.input {
    margin: 10px;
    font-size: 20px;   
}
.operation {
width: 40px;
height: 40px;
font-size: 30px;
margin: 10px;
 
}
</style>