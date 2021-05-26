<template>
  <div id="app">
   <div>
    <h3>当前最新的 count 值为：{{$store.state.count}}</h3>
    <h3>当前最新的 count 值为：{{$store.getters.showNum}}</h3>
    <button @click="add">+1</button>
    <button @click="addN">+N</button>
    <button @click="addAsync">+1 Async</button>
    <button @click="addNAsync">+N Async</button>
   </div>
  </div>
</template>

<script>
export default {
  data(){
    return {
      
    }
  },
  methods: {
    add(){
      this.$store.commit('add')
    },
    addN(){
      this.$store.commit('addN', 3)
    },
    addAsync(){
      this.$store.dispatch('addAsync')
    },
    addNAsync(){
      this.$store.dispatch('addNAsync', 4)
    }
  }
}
</script>
