<template>
  <div id="app">
   <img alt="Vue logo" src="./assets/logo.png"> 
   <HelloWorld msg="" :is-show="true"/>
    <Calc />
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue';
import Calc from './components/Calc.vue';

export default {
  name: 'App',
  components: {
    HelloWorld,
    Calc,
  },
  data() {
    return {
      counter: 0,
      str: 'Hello!',
    };
  },
  methods: {
    increase(step, event) {
      console.log(event);
      this.counter += step;
    },
    resetCounter() {
      this.counter = 0;
    },
    input(event) {
      console.log(event.target.value);
      this.str = event.target.value;
    },
    blur() {
      console.log('blur');
    },
    focus() {
      console.log('focus');
    },
  },
};
</script>

<style lang="css">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
