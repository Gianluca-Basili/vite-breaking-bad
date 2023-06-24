<script>
export default {
    
}
</script>
<template lang="">
    <div class="loader-wrapper">
        <div class="title-loader text"><h1><strong>pokémon</strong></h1></div>
        <div class="loader">
            <div><img src="https://www.gamesource.it/wp-content/uploads/2016/07/Pokeball.png" alt="" height="100" class="pakeball"></div>
        </div>

    </div>
</template>
<style lang="scss" scoped>

.loader-wrapper{
    position: fixed;
    top: 0;
    left: 0;
    width: 100vw;
    height: 100vh;
    background-color: white;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
}
    
.text{
    font-size: 30px;
    text-transform: uppercase;
}

.loader {
    border-radius: 50%;
    width: 120px;
    height: 120px;
    -webkit-animation: spin 2s linear infinite; /* Safari */
    animation: spin 2s linear infinite;
}
    
img{
    border-radius: 50%;
    
}

/* Safari */
@-webkit-keyframes spin {
  0% { -webkit-transform: rotate(0deg); }
  100% { -webkit-transform: rotate(360deg); }
}

@keyframes spin {
  0% { transform: rotate(0deg); }
  100% { transform: rotate(360deg); }
}
</style>