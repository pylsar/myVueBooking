<template>
    <div class="tab-info">
        <span class="tab-info__before-price">price starts as</span>
        <span class="tab-info__price">$ 8,500</span>
        <span class="tab-info__after-price">per room / night</span>
    </div>
</template>
<script>
export default{
    name: 'TabInfo'
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