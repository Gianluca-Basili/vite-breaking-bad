<script>
import appHeader from './components/appHeader.vue';
import appCharactersList from './components/appCharactersList.vue';

export default {
  components:{
    appHeader,
    appCharactersList,

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