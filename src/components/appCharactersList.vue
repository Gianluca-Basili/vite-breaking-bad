<script>

import appCharacterCard from './appCharacterCard.vue'
import { store } from '../store';
import appLoader from './appLoader.vue'
export default {
    components:{
        appCharacterCard,
        appLoader
        
    },
    data() {
        return {
            store
        }
    },
   
   
}
</script>
<template lang="">
    <div class="container character-container my-5">
        <div class="border">
            <div class="row" v-if="store.loading === false">
               
                <div v-for="(Character,index) in store.CharactersList"  class="col-6 col-md-4 col-lg-3">
                    <appCharacterCard :myCharacter="Character"/>
                </div>
            </div>
            
            <appLoader v-else />
        </div>
    </div>
</template>
<style lang="scss" scoped>
    .border{
        background-color: black;
        width: 100%;
    }

    .angle{
        border-radius: 10px;
    }
</style>