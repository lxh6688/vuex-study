<template>
  <div id="app">
   <div>
    <h3>当前最新的 count 值为：{{count}}</h3>
    <h3>当前最新的 count 值为：{{showNum}}</h3>
    <button @click="Sub">-1</button>
    <button @click="subN(3)">-N</button>
    <!-- <button @click="SubN">-N</button> -->
    <button @click="SubAsync">-1 Async</button>
    <button @click="subNAsync(3)">-N Async</button>
   </div>
  </div>
</template>

<script>
import { mapState, mapMutations, mapActions, mapGetters } from 'vuex'

export default {
  data(){
    return {
      
    }
  },
  computed: {
    ...mapState(['count']),
    ...mapGetters(['showNum']),
  },
   methods: {
     ...mapMutations(['sub', 'subN']),
     ...mapActions(['subAsync', 'subNAsync']),
    Sub(){
      this.sub()
    },
    SubN(){
      this.subN(3)
    },
    SubAsync(){
      this.subAsync()
    }
  }
}
</script>
