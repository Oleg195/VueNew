<template>
<div class="carousel-items">
    <img :src=" require('../views/images'+ item_data.img)" alt="">
</div>
</template>

<script>
export default{
    name:"carousel-items",
    props:{
        item_data:{
            type:Object,
            default:{}=>{}
        }
    },
    data{}{
        return{}
    },
    compited:{}
}
</script>
<style scoped>
</style>