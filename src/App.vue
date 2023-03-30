<script>
import axios from 'axios';
import { store } from '../store';
import MyHeader from './components/MyHeader.vue';
import MyMain from './components/MyMain.vue'
export default {
  data() {
    return {
      store
    }
  },
  components: {
    MyHeader,
    MyMain,

  },
  methods: {
    getCards() {
      this.store.loading = true;
      axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php')
        .then(response => {
          this.store.cardList = response.data.data;
          this.store.loading = false;
          console.log(this.store.cardList)
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
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
</style>



  