<script>
export default {
    
}
</script>
<template lang="">
    <div class="container">
        <button class="button" style="background-color:blue;"></button>
        <button class="button" style="background-color:red;"></button>
        <button class="button" style="background-color:yellow;"></button>
        <button class="button" style="background-color:green;"></button>

    </div>
</template>
<style lang="scss" scoped>
    .blue{
        padding: 10px;

    }
    
.button {
   
    border: none;
    color: white;
    padding: 20px;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 16px;
    margin: 4px 2px;
    border-radius: 50%;

    &:hover{
        padding: 20px;
        transition: transform .2s;
        width: 80px;
        height: 80px;
        margin: 0 auto;
    }

    
}




</style>