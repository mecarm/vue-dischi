<template>
  <div class="col-2 p-3 my-1 mx-3">
    <img class="w-100" :src="dettagliMusica.poster" alt="">
    <h5 class="pt-2">{{dettagliMusica.title}}</h5>
    <div>{{dettagliMusica.author}}</div>
    <span>{{dettagliMusica.year}}</span>
  </div>
</template>

<script>
export default {
  name: 'DischiComp',
  props: {
    dettagliMusica: Object
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.col-2{
  background: #303841;
  color: rgb(112, 107, 107);
}

h5{
  color: white;
}
</style>
