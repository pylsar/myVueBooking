<template>
    <section class="package">
        <div class="container">
            <h2 class="package__title">Other Packages</h2>  
            <card/>
        </div>

    </section>
</template>

<script>
import Card from './Card.vue'
export default{
    name: 'Package',
    components: { 
        Card
    },

}
</script>
<style lang="scss">
    .package{
        &__title{
            font-size: 36px;
            font-weight: 700;
            text-align: center;
            margin-bottom: 65px;
        }
    }
</style>