<template>
    <ul class="tabs">
        <li @click="tabClickSum">Total Sum</li>
        <li @click="tabClickMeal">Cost of Meal</li>
        <li @click="tabClickEx">Cost of Excursions</li>
        <li @click="tabClickTr">Cost of Transfers</li>
    </ul>
</template>
<script>
    export default{
        name: 'Tabs',
        methods:{
            tabClickSum(){
                this.$emit('tabClickSum')
            },
            tabClickMeal(){
                this.$emit('tabClickMeal')
            },
            tabClickEx(){
                this.$emit('tabClickEx')
            },
            tabClickTr(){
                this.$emit('tabClickTr')
            }
        }
    }
</script>
<style lang="scss">
.tabs{
    max-width: 60%;
    height: 80px;
    margin: 0 auto;
    display: flex;
    justify-content: center;
    align-items: center;
    & li {
        list-style: none;
        padding: 10px 20px;
        background: #0A223D;
        color: #fff;
        border-right: 3px solid lighten($color: #0A223D, $amount: 5);
        cursor: pointer;
        &:first-child{
            border-radius: 8px 0px 0px 8px;
        }
        &:last-child{
            border-right: none;
            border-radius: 0px 8px 8px 0px;
        }
        &:hover{
            opacity: .7;
        }
    }
}
</style>