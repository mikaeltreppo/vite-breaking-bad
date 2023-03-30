<template>
    <div class="card">
     <img :src="immagine">
<h3>{{ name }}</h3>
</div>
</template>


<style>

.card{
    width: calc(100% / 5);
}
img{
    max-width: 100%;
}

</style>


<script>   
export default {
    name: 'MyCard',
    props: {
        immagine: String,
        name: String
      
    }
}

</script>