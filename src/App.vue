<template>
  <div id="app">
    <h1>2 way binding</h1>
    <input type="text" v-model="inputText">
    <p>inputText {{ inputText }}</p>
    <br>
    <p>radio buttons must share the same model, and use value instead of name attributes</p>
    <input type="radio" v-model="value" value="one">one
    <input type="radio" v-model="value" value="two">two
    <input type="radio" v-model="value" value="three">three
    <br>
    {{ value }}
    <br>
    <p>html can be written to the page unescaped using v-html</p>
    <div v-html="yourHTML"></div>
  </div>
</template>

<script>

export default {
  name: 'app',
  data() {
    return {
      inputText: 'initial value',
      value: 'one',
      yourHTML: '<h1>2 way binding</h1>'
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
