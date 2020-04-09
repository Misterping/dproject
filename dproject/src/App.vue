<template>
  <div id="app">
    <Index />
   <!-- <router-view/> -->
  </div>
</template>

<script>
import Index from './components/Index'
export default {
  name:'App',
  components:{
    Index,
  },
  data () {
    return {
      msg: ''
    }
  }
   
}
</script>

<style>
  body,html{
  width:100%;
  height:100%;
  margin:0px;
}
#app{
  width:100%;
  height: 100%;
}
</style>
