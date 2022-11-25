<template>
  <div id="app">
    <header>
      <div>
        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/19/Spotify_logo_without_text.svg/2048px-Spotify_logo_without_text.svg.png" alt="">
      </div>
      
    </header>
    <DischiComp/>
  </div>
</template>

<script>
import DischiComp from './components/DischiComp.vue'

export default {
  name: 'App',
  components: {
    DischiComp
  }
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  height: 100vh;
}
header{
  background-color: #273039;
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
