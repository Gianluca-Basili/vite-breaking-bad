<script>
import axios from 'axios';
import appHeader from './components/appHeader.vue';
import appCharactersList from './components/appCharactersList.vue';
import appSearch from './components/appSearch.vue';
import { store } from './store';

export default {
  components:{
    appHeader,
    appCharactersList,
    appSearch,

  },

  data(){
    return{
      store,
      

    }
  },
  mounted(){
    this.getCharacters()
  },
  methods:{
    getCharacters(){
     
      let myUrl = store.apiUrl;

      if(store.searchText !== ''){
        myUrl += `?q[name]=${store.searchText}`;
      }

      if(store.statusValue !==''){
        if(store.searchText !== ''){
          myUrl += '&';   
        }

        else{
          myUrl +='?';
        }

        myUrl +=`eq[type1]=${store.statusValue}`;
      }
      axios.get(myUrl).then((response) =>{
      store.CharactersList = response.data.docs;
      store.loading = false;
        
      })
      
    }
  }
}
</script>
<template lang="">
  <div>
    <appHeader />
    <appSearch @search="getCharacters"/>
    <appCharactersList />
  </div>
</template>
<style lang="scss">
  @use './styles/general.scss' as *;
</style>