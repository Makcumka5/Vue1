<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" />
    <!-- <Calculator /> -->

    <hr />

    <calculator v-if="Calculator" />
    <button @click="Calculator = !Calculator">Calc</button>
  </div>
</template>

<script>
import Calculator from "./components/Calculator.vue";
export default {
  name: "App",

  data() {
    return {
      Calculator: null,
    };
  },
  //  methods: {
  //     onMouseOver () {
  //       console.log('Hovered on button!')
  //     }
  //   },
  //   mounted () {
  //     const btn = this.$el.querySelector('button')
  //     if (btn) {
  //       btn.addEventListener('mouseover', this.onMouseOver)
  //     }
  //   }
  // beforeDestroy() {
  //   const btn = this.$el.querySelector("button");
  //   if (btn) {
  //     btn.removeEventListener("onmouseover", this.onHover);
  //   }
  // },

  components: {
    Calculator,
  },
};
</script>

<style lang="scss" scoped>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
