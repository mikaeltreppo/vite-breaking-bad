<template></template>
<div :src="image">
</div>
<style></style>
<script>   export default {
    name: 'MyCard',
    props: {
        name: String,
        image: String
    }
}

</script>