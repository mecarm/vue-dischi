<template>
  <header class="d-flex align-items-center justify-content-between">
    <div>
      <img
        src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/19/Spotify_logo_without_text.svg/2048px-Spotify_logo_without_text.svg.png"
        alt="">
    </div>
    <div class="w-25 me-3">
      <select class="form-select" v-model="genereSelezionato" @change="$emit('emitGenere', genereSelezionato)" aria-label="Default select example">
        <option disabled value="">Filtra per genere</option>
        <!-- Ciclo l'array ricevuto tramite props -->
        <option :value="elem" v-for="(elem, index) in PropsArrayGeneri" :key="index">{{elem}}</option>
      </select>
    </div>
  </header>
</template>

<script>
export default {
    name: 'HeaderComp',
    props: {
      PropsArrayGeneri : Array
    },
    data(){
      return{
        genereSelezionato: ''
      }
    }
}
</script>

<style lang="scss" scoped>
header{
  background-color: #303841;
  height: 10%;

  div{
    width: 50px;
    height: 100%;
    display: flex;
    align-items: center;
    margin-left: 10px;
  }

  img{
    width: 100%;
  }
}
</style>