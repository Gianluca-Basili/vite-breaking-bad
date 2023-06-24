<script>
import axios from 'axios';
import appHeader from './components/appHeader.vue';
import appCharactersList from './components/appCharactersList.vue';
import { store } from './store';

export default {
  components:{
    appHeader,
    appCharactersList,

  },

  data(){
    return{
      store,
      

    }
  },
  mounted(){
    axios.get(store.apiUrl).then((response) =>{
      store.CharactersList = response.data.docs;
      store.loading = false
        
    })
  }
}
</script>
<template lang="">
  <div>
    <appHeader />
    <appCharactersList />
  </div>
</template>
<style lang="scss">
  @use './styles/general.scss' as *;
</style>