<template>
<div class="container">
    <div class="showCardContainer">
      <MyListCard></MyListCard>
    </div>
</div>

</template>

<style>
.container{
    background-color: rgb(212, 143, 56);
    
    padding: 30px;
}
.showCardContainer{
    background-color: white;
    width: 80%;
    margin: auto;
   
}
</style>

<script>
import MyListCard from './MyListCard.vue'
import { store } from '../../store';
export default {
    data(){
        return{
            store
        }
    },
    components:{
        MyListCard

    }
}
</script>