<template>
    <div>
        <div v-if="currentTab === 0" class="tab-info">
            <span class="tab-info__before-price">price starts as</span>
            <span class="tab-info__price">$ 8,500</span>
            <span class="tab-info__after-price">per room / night</span>
        </div>
        <div v-if="currentTab === 1" class="tab-info">
            <span class="tab-info__before-price">price of meal</span>
            <span class="tab-info__price">$ 1,200</span>
            <span class="tab-info__after-price">only dinner</span>
        </div>
        <div v-if="currentTab === 2" class="tab-info">
            <span class="tab-info__before-price">excursions</span>
            <span class="tab-info__price">$ 1,600</span>
            <span class="tab-info__after-price">3 or more</span>
        </div>
        <div v-if="currentTab === 3" class="tab-info">
            <span class="tab-info__before-price">transfers</span>
            <span class="tab-info__price">$ 700</span>
            <span class="tab-info__after-price">airport/hotel</span>
        </div>
    </div>
    
</template>
<script>
export default{
    name: 'TabInfo',
    props: {
        currentTab: {
            type: Number,
        },
    },
}
</script>
<style lang="scss">
.tab-info{
    display: flex;
    flex-direction: column;
    &__before-price{
        font-size: 10px;
    }
    &__price{
        font-size: 24px;
        font-weight: 700;
    }
    &__after-price{
        font-size: 12px;
    }
}
</style>