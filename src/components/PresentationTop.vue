<template>
    <div class="presentationtop">
        <div class="presentationtop__left">
            <div class="presentationtop__left-star">
                <span>&#9733;</span>
                <span>&#9733;</span>
                <span>&#9733;</span>
                <span>&#9733;</span>
                <span>&#9733;</span>
            </div>
            <div class="presentationtop__left-title">
                <h2>GRAND HILTON HOTEL</h2>
                <button>Flash Offer</button>    
            </div>
            <p class="presentationtop__left-text">Half-Board/ All Inclusive + Complimentary Activities + Child Stays Free</p>
        </div>
        <div class="presentationtop__right">
            <span class="presentationtop__right-text">User Rattings</span>
            <span>4.5/<small>5</small></span>
        </div>
    </div>
</template>
<script>
export default{
    name: 'PresentationTop',
}
</script>
<style lang="scss">
@import '../main.scss';
.presentationtop{
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 100px;
    &__left-star{
        color: #F2994A;
    }
    &__left-title{
        display: flex;
        & h2 {
            margin-right: 14px;
        }
        & button {
            color: #fff;
            background: #EC1F46;
            font-size: 10px;
            line-height: 1;
            outline: none;
            border: none;
            padding: 4px 9px;
            border-radius: 6px;
        }
    }
    &__left-text{
        font-size: 12px;
        margin-top: 4px;
    }
    &__right{
        display: flex;
        flex-direction: column;
        align-items: center;
        background: #EC1F46;
        padding: 8px;
        border-radius: 6px;
        color: #fff;
        & small {
            font-size: 10px;
        }
    }
    &__right-text{
        font-size: 8px;
    }
}
</style>