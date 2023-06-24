<script>
import axios from 'axios';
import appCharacterCard from './appCharacterCard.vue'


export default {
    components:{
        appCharacterCard
        
    },
    data(){
        return{
            CharactersList:[]

        }
    },
    mounted(){
        axios.get('https://41tyokboji.execute-api.eu-central-1.amazonaws.com/dev/api/v1/pokemons?eq[type1]=Electric&sort[number]=desc').then((response) =>{
            this.CharactersList = response.data.docs;
            
        })
    }
}
</script>
<template lang="">
    <div class="container character-container my-5">
        <div class="row">
            <div v-for="(Character,index) in CharactersList"  class="col-6 col-md-4 col-lg-3">
                <appCharacterCard :myCharacter="Character"/>
            </div>
        </div>
    </div>
</template>
<style lang="">
    
</style>