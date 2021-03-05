<template>
  <div id="app">
    <input v-model.number="num1" type="number">
    <span>+</span>
    <input v-model.number="num2" type="number">
    <span>=</span>
    <span>{{ num1 + num2 }}</span>
    
    <div>
      <select v-model="name">
        <option>Bilaal</option>
        <option>Bryson</option>
        <option>Cesca</option>
        <option>Jeff</option>
        <option>Maya</option>
        <option>Matt</option>
        </select>
        <p v-if="name">{{name}}</p>
        </div>
        <br>
        <Watcher />
    </div>
</template>

<script>
import Watcher from './components/Watcher'

export default {

  name: 'App',
  data() {
    return {
      num1: 0,
      num2: 0,
      name: ''
    }
  },
    components: {
    Watcher
  }
 
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
