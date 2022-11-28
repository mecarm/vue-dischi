<template>
  <div id="app">

    <HeaderComp @emitGenere='methodsGenereSelected' :PropsArrayGeneri='arrayGeneri'/>

    <MainComp @emitGeneri='mehodsListaGeneri' :PropsGenereSelezionato='genereValue'/>

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
      genereValue: '',
      arrayGeneri: []
    }
  },
  methods: {
    methodsGenereSelected(valueRiportatoDaHeader){
      this.genereValue = valueRiportatoDaHeader
    },
    //richiamo funzione nell'emit nel template per associare il valore dell arraygeneri nel main al arrayGeneri creato qui in app.vue
    mehodsListaGeneri(valueRicevutoNellEmit){
      this.arrayGeneri = valueRicevutoNellEmit
    }
  },
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
