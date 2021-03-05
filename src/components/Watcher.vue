<template>
  <div class="hello">
    <button @click="getPizza">Click me to order Pizza</button>
    <h2>Where is my Pizza?</h2>
    <h2>{{orderStatus}}</h2>
    <p v-if="orderSubmitted">{{orderSubmitted}}</p>
  </div>
</template>

<script>
export default {
  name: 'Watcher',
  data() {
    return {
      orderStatus: '',
      orderSubmitted: null
    }
  }, 
    methods:{
      getPizza() {
        this.orderStatus = "🍕"
      }
    }, 
    watch: {
      orderStatus() {
        this.orderSubmitted = "your order was submitted"

        setTimeout(() => this.orderSubmitted = null, 1000)
      }
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
