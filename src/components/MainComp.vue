<template>
  <main class="overflow-auto">
    <div class=" cards d-flex flex-wrap">
        <DischiComp v-for="(element, index) in dataMusic" :key="index" :dettagliMusica="element"/>
    </div>
  </main>
</template>

<script>
import axios from 'axios';
import DischiComp from './DischiComp.vue';

export default {
    name: 'MainComp',
    components: {
        DischiComp,
    },
    data(){
        return{
            dataMusic: '',
        }
    },
    mounted(){
        axios.get('https://flynn.boolean.careers/exercises/api/array/music')
            .then( (response) => {
                this.dataMusic = response.data.response
    })
    }
}
</script>

<style lang="scss" scoped>

main{
    height: 90%;
    background: #1D2E3C;
    padding: 30px;
}

.cards{
    width: 80%;
    margin: auto;
}
</style>