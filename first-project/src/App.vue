<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    
        <HelloWorld msg="My Calc" />
    <Calculator />

  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Calculator from './components/Calculator.vue'
export default {
  name: 'App',
  components: {
    HelloWorld,
    Calculator
  },
  data(){
    return {
      count: 0, 
      currentDate: 0,
      message: "Hello Vue",    
    }
  },
  // computed: {
  //   computedDate(){
  //     return this.currentDate || "Текущая дата"
  //   }
  // }
}
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

.data{
  font-size: 20px;
}
</style>
