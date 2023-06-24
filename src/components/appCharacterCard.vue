<script>
export default {
    props:{
        myCharacter: Object
    }
}
</script>
<template lang="">
    <div class="text-center">
        <div class="electric my-2">
            <img :src="myCharacter.imageUrl" clss="img-fluid mb-3 " :alt="myCharacter.info" height="200" width="200"/>
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
</style>


        

        