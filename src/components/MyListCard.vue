<template>
                   <MyCard 
                    :name="this.store.cardList.name" 
                />
</template>
<style></style>
<script>

import { store } from '../../store.js';
import MyCard from './MyCard.vue'
export default {
    data() {
        return {
            MyCard,
            store
        }
    },
    components: {
        CharacterCard
    }
}
</script>