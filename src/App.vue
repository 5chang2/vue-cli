<template>
  <div id="app">
    <div>
      <button @click="statusIndex">Index</button>
      <button @click="statusLotto">Lotto</button>
      <button @click="statusLunch">Lunch</button>
    </div>
    <Index v-if="status == 'index'"/>
    <Lunch v-if="status == 'lunch'"/>
    <Lotto v-if="status == 'lotto'"/>
  </div>
</template>

<script>
import Index from './components/Index.vue'
import Lunch from './components/Lunch.vue'
import Lotto from './components/Lotto.vue'

export default {
  name: 'App',
  components: {
    Lunch,
    Lotto,
    Index,
  },
  data: function(){
    return {
      status: 'index',
    }
  },
  methods: {
    statusLunch(){
      this.status = 'lunch'
    },
    statusLotto(){
      this.status = 'lotto'
    },
    statusIndex(){
      this.status = 'index'
    }
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
