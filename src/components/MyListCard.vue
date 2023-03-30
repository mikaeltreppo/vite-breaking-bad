<template>
                 <div class="d-flex" v-if="store.loading == false">
                    <MyCard v-for="(card,index) in store.cardList" :immagine="card.card_images[0].image_url" :type="card.archetype" :name="card.name" :key='index'></MyCard>
                </div>  
                 <div v-else>La pagina sta caricando</div>
</template>













<style>
.d-flex{
    display:flex;
    justify-content: space-around;
    flex-wrap: wrap;
}
</style>
<script>

import { store } from '../../store.js';
import MyCard from './MyCard.vue'
export default {
    data() {
        return {
            store
        }
    },
    components: {
    MyCard
    }
}
</script>