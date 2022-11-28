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
    props: {
        PropsGenereSelezionato: String
    },
    components: {
        DischiComp,
    },
    data(){
        return{
            dataMusic: '',
            arrayGeneri: []
        }
    },
    //Con la funzione computed posso attivare il filter al cambiamento della variabile PropsGenereSelezionato
    computed:{

    },
    mounted() {
        axios.get('https://flynn.boolean.careers/exercises/api/array/music')
            .then((response) => {
                this.dataMusic = response.data.response

                this.dataMusic.forEach(elem => {

                    if (!this.arrayGeneri.includes(elem.genre)) {
                        this.arrayGeneri.push(elem.genre)
                    }
                })
                this.$emit('emitGeneri', this.arrayGeneri)
            });

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