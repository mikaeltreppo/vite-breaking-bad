<script>
import axios from 'axios';
import {store} from '../store.js';
import MyHeader from './components/MyHeader.vue';
import MyMain from'./components/MyMain.vue'
export default {
    data() {
      return {
        MyHeader,
        MyMain,
        store
      }
    },
    methods: {
      getCards() {
        axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?format=Speed Duel')
        .then(response => {
            console.log(response)
    
        });
      }
    },
    created() {
      this.getCards();
    }
  }



</script>

<template>
  <MyHeader></MyHeader>
  <MyMain></MyMain>

</template>

<style scoped></style>



  