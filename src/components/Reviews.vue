<template>
    <section class="reviews container">
        <h2 class="reviews__title">What people thinks about us</h2>
        <reviews-card />
    </section>
</template>  
<script>
import ReviewsCard from './ReviewsCard.vue'
export default {
    name: 'Reviews',
  components: { 
      ReviewsCard 
    },

}
</script>

<style lang="scss">
.reviews{
    &__title{
        font-size: 36px;
        font-weight: 700;
        text-align: center;
        margin-bottom: 65px;
    }
}
</style>