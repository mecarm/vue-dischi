<template>
  <div id="app">
    <HeaderComp @emitGenere='genereInMethods'/>
    <MainComp/>
  </div>
</template>

<script>
import HeaderComp from './components/HeaderComp.vue'
import MainComp from './components/MainComp.vue'

export default {
  name: 'App',
  components: {
    HeaderComp,
    MainComp,
  },
  data(){
    return{
      genereValue: ''
    }
  },
  methods: {
    genereInMethods(valueRiportatoDaHeader){
      this.genereValue = valueRiportatoDaHeader
    }
  }
}
</script>

<style lang="scss">
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  height: 100vh;
}
</style>
