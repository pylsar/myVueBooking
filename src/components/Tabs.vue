<template>
    <ul class="tabs">
        <li @click="tabClickSum">
            <span v-if="mobile">Sum</span>
            <span v-else>Total Sum</span>
        </li>
        <li @click="tabClickMeal">
            <span v-if="mobile">Meal</span>
            <span v-else>Cost of Meal</span>
        </li>
        <li @click="tabClickEx">
            <span v-if="mobile">Excursion</span>
            <span v-else>Cost of Excursions</span>
        </li>
        <li @click="tabClickTr">
           <span v-if="mobile">Transfer</span>
           <span v-else> Cost of Transfers</span>
        </li>
    </ul>
</template>
<script>
    export default{
        name: 'Tabs',
        data(){
            return{
                mobile: false
            }
        },
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
            },
            onResize() {
                this.mobile = window.innerWidth <= 640;
            }
        },
        created() {
            //отслеживаем ресайз экрана
            window.addEventListener('resize', this.onResize);
            this.onResize();
        },
          destroyed() {
              //не уверен что надо
            window.removeEventListener('resize', this.onResize)
        },
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

@media screen and (max-width: 1024px) {
    .tabs{
        max-width: 80%;
    }
}
@media screen and (max-width: 768px) {
    .tabs{
        max-width: 100%;
    }
}
@media screen and (max-width: 640px) {
    .tabs{
        max-width: 100%;
        & li {
            padding: 10px 10px;
        }
    }
}
</style>