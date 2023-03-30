<template>
    <div class="card">
        <img :src="immagine">
        <h3>{{ name }}</h3>
        <h5>{{ type }}</h5>
    </div>
</template>


<style>
.card {
      width: calc(100% / 5);
    text-align: center;
    margin: 10px;
background-color: rgb(212, 143, 56);
}
h3{
    display: inline-block;
    height: 80px;    
}
h5{
    color: rgb(78, 44, 44);
}

img {
    max-width: 100%;
}
</style>


<script>
export default {
    name: 'MyCard',
    props: {
        immagine: String,
        name: String,
        type: String

    }
}

</script>