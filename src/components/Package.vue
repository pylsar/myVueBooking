<template>
    <section class="package container">
        <h2 class="package__title">Other Packages</h2>  
        <card/>
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
        padding-bottom: 42px;
        &__title{
            font-size: 36px;
            font-weight: 700;
            text-align: center;
            margin-bottom: 65px;
        }
    }
    @media screen and (max-width: 768px) {
        .package{
        padding-bottom: 24px;
        &__title{
            font-size: 24px;
            margin-bottom: 24px;
        }
    }
    }
</style>