<script>
import axios from 'axios';
import { store } from '../store.js';
import MyHeader from './components/MyHeader.vue';
import MyMain from './components/MyMain.vue'
export default {
  data(){
    return{
      store
    }
  },
    components:{
        MyHeader,
        MyMain,
       
      },
  methods: {
    getCards() {
      axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?archetype=Blue-Eyes')
        .then(response => {
          this.store.cardList = response.data.data;
          for(let i = 0; i< this.store.cardList.length; i++){
          console.log(this.store.cardList[i].name)
          }

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



  