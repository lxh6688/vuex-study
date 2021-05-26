<template>
  <div>
    <Addition></Addition>
    <Subtraction></Subtraction>
  </div>
</template>

<script>
import Addition from './components/Addition'
import Subtraction from './components/Subtraction'

export default {
  name: 'App',
  components: {
    Addition,
    Subtraction
  },
  data(){
    return {

    }
  }
}
</script>
