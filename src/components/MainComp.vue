<template>
  <main>
    <div class="row">
        <DischiComp v-for="n in 10" :key="n"/>
    </div>
  </main>
</template>

<script>
import DischiComp from './DischiComp.vue'

export default {
    name: 'MainComp',
    components: {
        DischiComp,
    }
}
</script>

<style lang="scss" scoped>

main{
    height: 90%;
    background: #1D2E3C;
    padding: 20px;
}

.row{
    width: 80%;
    margin: auto;
    justify-content: center;
}
</style>