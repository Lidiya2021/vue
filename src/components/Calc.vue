<template>
  <div>
    <div>
      <input class="op" type="number" v-model.number="op1">
      <input class="op" type="number" v-model.number="op2">
      = <span class="rez">{{ result }}</span>
    </div>
    <div>
      <button class="result" @click="result = op1 + op2">+</button>
      <button class="result" @click="sub">-</button>
      <button class="result" @click="div">/</button>
      <button class="result" @click="mult">*</button>
      <button class="result" @click="degree">х<sup>2</sup></button>
      <button class="result" @click="remains">1/x</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Calc',
  data: () => ({
    op1: 0,
    op2: 0,
    result: 0,
  }),
  methods: {
    sub() {
      this.result = this.op1 - this.op2;
    },
    div() {
      this.result = this.op1 / this.op2;
    },
    mult() {
      this.result = this.op1 * this.op2;
    },
    degree() {
      this.result =  Math.pow(this.op1, this.op2);
    },
    remains() {
      this.result =  parseInt(this.op1 / this.op2);
    },
   
  },
};
</script>

<style lang="css">
.op, 
.result {
    margin-bottom : 25px;
    margin-left: 10px;
    width: 50px;
    height: 50px;
    text-align: center;
    font-size: 15px;
}
.rez {
  font-size: 15px;
}


</style>