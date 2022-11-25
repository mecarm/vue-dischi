<template>
    <header>
        <div>
            <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/19/Spotify_logo_without_text.svg/2048px-Spotify_logo_without_text.svg.png"
                alt="">
        </div>
    </header>
</template>

<script>
export default {
    name: 'HeaderComp'
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