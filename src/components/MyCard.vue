<template>
    <h3>{{ name }}</h3>
</template>


<style></style>


<script>   
export default {
    name: 'MyCard',
    props: {
        name: String,
        image: String,
        type: String
    }
}

</script>