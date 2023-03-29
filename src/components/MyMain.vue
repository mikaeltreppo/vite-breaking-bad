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
    height: 2000px;
    padding: 30px;
}
.showCardContainer{
    background-color: white;
    width: 80%;
    margin: auto;
    height: 1000px;
}
</style>

<script>
import MyListCard from './MyListCard.vue'
export default {
    components:{
        MyListCard

    }
}
</script>