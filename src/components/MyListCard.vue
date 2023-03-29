<template>
                 <div><MyCard></MyCard></div>  
</template>













<style></style>
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