<script>
export default {
    props:{
        myCharacter: Object
    }
}
</script>
<template lang="">
    <div class="text-center">
        <div class="electric my-4">
            <img :src="myCharacter.imageUrl" class=" my-3" :alt="myCharacter.info" height="200" width="200"/>
            <div class="code">
                {{myCharacter.code}}
            </div>
            <h4><strong>{{myCharacter.name}}</strong></h4>
            {{myCharacter.type1}}
        </div>
    </div>
</template>
<style lang="scss" scoped>
    img{
        border-radius: 50%;
        
    }

    .electric{
        background-color:rgb(241, 254, 96);
        border-radius: 10px;
        width: 90%;
        margin: 0 auto;
       
    }

</style>


        

        