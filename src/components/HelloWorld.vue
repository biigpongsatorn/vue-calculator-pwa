<template>
  <div class="hello">
    <h3>{{ msg }}</h3>
    <input type="number" v-model="firstNum">
    <div class="plus">
      +
    </div>
    <input type="number" v-model="secNum">
    <div>
      <h1 class="result">
        Result: {{ parseInt(firstNum ? firstNum : 0) + parseInt(secNum ? secNum : 0) }}
      </h1>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator'

@Component
export default class HelloWorld extends Vue {
  @Prop() private msg!: string;
  private firstNum = 0;
  private secNum = 0
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 20px 0;
}
input {
  padding: 10px;
  border: 1px solid #e5e5e5;
  border-radius: 5px;
  font-size: 27px;
  text-align: center;
}
.plus {
  font-size: 27px;
  text-align: center;
  margin: 10px 0;
}
.result {
  color: green;
}
</style>
