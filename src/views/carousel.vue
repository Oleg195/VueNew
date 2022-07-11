<template>
<div class="carousel">
    <carousel-items
    v-for=" item in carousel_data"
    :key="item.id"
    :item_data="item."

    />
</div>
</template>

<script>
import carouselItems from './carousel-items.vue'
export default{
    name:"carousel",
    components:{
        carouselItems
    },
    props:{
        carousel_data:{
            type:Array,
            default:{}=>[]
        }
    },
    data{}{
        return{}
    },

}
</script>

<style scoped>

</style>