<script>
import {store} from '../store.js';
export default {
    data() {
        return {
            store,
            types:[
                "Bug",
                "Dark",
                "Dragon",
                "Electric",
                "Fairy",
                "Fighting",
                "Fire",
                "Flying",
                "Ghost",
                "Grass",
                "Ground",
                "Ice",
                "Normal",
                "Poison",
                "Psychic",
                "Rock",
                "Steel",
                "Water"
            ]
        }
    
    },
    methods:{
       
        
    }
}
</script>
<template lang="">
    <div>
        <div class="container">
            <div class="row">
                <div class="col-6 offset-3 ">
                    <div class="d-flex my-4">
                        <input type="text" v-model="store.searchText" class="input-control me-2" placeholder="cerca pokèmon" @keyup.enter="$emit('search')">
                        <select name="" id="" class="form-control me-2" v-model="store.statusValue">
                            <option value="" selected>select types</option>
                            <option value="" v-for="(type,index) in types" :key="index" :value="type">{{type}}</option>
                        </select>
                        <button class="btn btn-sm btn-primary" @click="$emit('search')">cerca</button>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<style lang="scss" scoped>
    
</style>
                            


