<script>
import axios from 'axios';
import { store } from '../store.js';
import MyHeader from './components/MyHeader.vue';
import MyMain from './components/MyMain.vue'
export default {
    components:{
        MyHeader,
        MyMain,
        store
      },
  methods: {
    getCards() {
      axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?archetype=Blue-Eyes')
        .then(response => {
          console.log(response.data.data)

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

<style>
*{
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}</style>



  