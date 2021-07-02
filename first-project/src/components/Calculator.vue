<template>
  <section class="calc">
    <h2>Калькулятор</h2>
    <div class="inputs">
      <input type="number" v-model.number.trim="num1" />
      {{ symbol }}
      <input type="number" v-model.number.trim="num2" />
      = {{ result }}
    </div>
    <div class="buttons">
      <button @click="sum">+</button>
      <button @click="diff">-</button>
      <button @click="mult">*</button>
      <button @click="div">/</button>
    </div>
    <input id="num1" type="radio" v-model="picked" value="1" />
    <input id="num2" type="radio" v-model="picked" value="2" />

    <div>
      <button class="operation" @click="numFunc(n)" v-for="n in 9" :key="n">
        {{ n }}
      </button>
      <button class="operation" @click="delNum()">!</button>
    </div>
  </section>
</template>

<script>
export default {
  name: "Calculator",
  data() {
    return {
      num: "",
      num1: "",
      num2: "",
      result: "?",
      symbol: " ? ",
      picked: "1",
    };
  },
  methods: {
    sum() {
      this.result = +this.num1 + +this.num2;
      this.symbol = " + ";
    },
    diff() {
      this.result = +this.num1 - +this.num2;
      this.symbol = " - ";
    },
    mult() {
      this.result = +this.num1 * +this.num2;
      this.symbol = " * ";
    },
    div() {
      this.result = +this.num1 / +this.num2;
      this.symbol = " / ";
    },
    numFunc(num) {
      if (+this.picked === 1) {
        this.num1 += num.toString();
      } else if (+this.picked === 2) {
        this.num2 += num.toString();
      }
    },
    delNum() {
      if (+this.picked === 1)
        this.num1 = this.num1.substring(0, this.num1.length - 1);
      else if (+this.picked === 2)
        this.num2 = this.num2.substring(0, this.num2.length - 1);
    },
  },
};
</script>

<style lang="sass">
.section
    padding-top: 12px
    padding-bottom: 12px

.buttons
    padding-top: 12px
    padding-bottom: 12px
.operation
    margin: 3px
    font-size: 30px
</style>
