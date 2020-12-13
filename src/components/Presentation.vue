<template>
    <div class="container">
        <section class="presentation">
            <presentation-top />
            <div class="presentation__content">
                <div class="presentation__content-left">
                    <img src="../assets/img/1.png" alt="hilton">
                </div>
                <div class="presentation__content-right">
                    <div class="presentation__content-info">
                        <div class="presentation__content-top">
                            <div class="presentation__content-top--left">
                                <tab-info :currentTab="currentTab"/>
                            </div>
                            <div class="presentation__content-top--right">
                                <div class="presentation__icon-box">
                                    <svg width="14" height="14" viewBox="0 0 14 14" fill="none" xmlns="http://www.w3.org/2000/svg">
                                         <path fill-rule="evenodd" clip-rule="evenodd" d="M2.60427 9.02094C3.15125 8.47396 3.89312 8.16666 4.66667 8.16666H9.33333C10.1069 8.16666 10.8487 8.47396 11.3957 9.02094C11.9427 9.56792 12.25 10.3098 12.25 11.0833V12.25C12.25 12.5722 11.9888 12.8333 11.6667 12.8333C11.3445 12.8333 11.0833 12.5722 11.0833 12.25V11.0833C11.0833 10.6192 10.899 10.1741 10.5708 9.84589C10.2426 9.51771 9.79746 9.33333 9.33333 9.33333H4.66667C4.20254 9.33333 3.75742 9.51771 3.42923 9.84589C3.10104 10.1741 2.91667 10.6192 2.91667 11.0833V12.25C2.91667 12.5722 2.6555 12.8333 2.33333 12.8333C2.01117 12.8333 1.75 12.5722 1.75 12.25V11.0833C1.75 10.3098 2.05729 9.56792 2.60427 9.02094Z" fill="white"/>
                                         <path fill-rule="evenodd" clip-rule="evenodd" d="M6.99992 2.33333C6.03342 2.33333 5.24992 3.11683 5.24992 4.08333C5.24992 5.04983 6.03342 5.83333 6.99992 5.83333C7.96642 5.83333 8.74992 5.04983 8.74992 4.08333C8.74992 3.11683 7.96642 2.33333 6.99992 2.33333ZM4.08325 4.08333C4.08325 2.4725 5.38909 1.16666 6.99992 1.16666C8.61075 1.16666 9.91659 2.4725 9.91659 4.08333C9.91659 5.69416 8.61075 7 6.99992 7C5.38909 7 4.08325 5.69416 4.08325 4.08333Z" fill="white"/>
                                    </svg>
                                    <span>2 x Guests</span>
                                </div>
                                <div class="presentation__icon-box">
                                    <svg width="14" height="14" viewBox="0 0 14 14" fill="none" xmlns="http://www.w3.org/2000/svg">
                                        <path fill-rule="evenodd" clip-rule="evenodd" d="M6.64195 0.70621C6.8526 0.542373 7.14757 0.542373 7.35821 0.70621L12.6082 4.78954C12.7503 4.90006 12.8334 5.06999 12.8334 5.25V11.6667C12.8334 12.1308 12.649 12.5759 12.3209 12.9041C11.9927 13.2323 11.5475 13.4167 11.0834 13.4167H2.91675C2.45262 13.4167 2.0075 13.2323 1.67931 12.9041C1.35112 12.5759 1.16675 12.1308 1.16675 11.6667V5.25C1.16675 5.06999 1.24986 4.90006 1.39195 4.78954L6.64195 0.70621ZM2.33341 5.5353V11.6667C2.33341 11.8214 2.39487 11.9697 2.50427 12.0791C2.61367 12.1885 2.76204 12.25 2.91675 12.25H11.0834C11.2381 12.25 11.3865 12.1885 11.4959 12.0791C11.6053 11.9697 11.6667 11.8214 11.6667 11.6667V5.5353L7.00008 1.90567L2.33341 5.5353Z" fill="white"/>
                                        <path fill-rule="evenodd" clip-rule="evenodd" d="M4.66675 7C4.66675 6.67783 4.92792 6.41667 5.25008 6.41667H8.75008C9.07225 6.41667 9.33342 6.67783 9.33342 7V12.8333C9.33342 13.1555 9.07225 13.4167 8.75008 13.4167C8.42792 13.4167 8.16675 13.1555 8.16675 12.8333V7.58333H5.83342V12.8333C5.83342 13.1555 5.57225 13.4167 5.25008 13.4167C4.92792 13.4167 4.66675 13.1555 4.66675 12.8333V7Z" fill="white"/>
                                    </svg>
                                    <span>1 x Room</span>
                                </div>
                            </div>
                        </div>
                        <div class="presentation__content-top--bottom">
                            <span>Quick Booking</span>
                            <div class="presentation__icon-box">
                                <svg width="14" height="14" viewBox="0 0 14 14" fill="none" xmlns="http://www.w3.org/2000/svg">
                                    <g clip-path="url(#clip0)">
                                    <path d="M11.6666 13.3583C11.6083 13.3583 11.5499 13.3583 11.4916 13.3583C9.62494 13.125 7.75827 12.4833 6.18327 11.4917C4.72494 10.5583 3.4416 9.275 2.50827 7.81667C1.45827 6.24167 0.816602 4.375 0.641602 2.50833C0.641602 2.04167 0.758268 1.575 1.04993 1.225C1.3416 0.875 1.74993 0.641667 2.2166 0.583333C2.27493 0.583333 2.33327 0.583333 2.3916 0.583333H4.1416C5.0166 0.583333 5.77494 1.225 5.8916 2.1C5.94994 2.625 6.0666 3.15 6.2416 3.61667C6.47493 4.25833 6.29994 4.95833 5.83327 5.48333L5.42494 5.89167C6.12494 6.94167 6.99993 7.875 8.10827 8.575L8.5166 8.16667C8.98327 7.7 9.7416 7.525 10.3833 7.75833C10.8499 7.93333 11.3749 8.05 11.8999 8.10833C12.7749 8.225 13.4166 8.98333 13.4166 9.85833V11.6083C13.4166 12.075 13.2416 12.5417 12.8916 12.8333C12.5416 13.125 12.1333 13.3583 11.6666 13.3583ZM4.1416 1.75H2.3916C2.2166 1.75 2.0416 1.86667 1.92493 1.98333C1.8666 2.1 1.80827 2.21667 1.80827 2.39167C1.98327 4.08333 2.5666 5.71667 3.49994 7.175C4.37494 8.51667 5.48327 9.68333 6.82493 10.5C8.28327 11.4333 9.9166 12.0167 11.6083 12.1917C11.8416 12.1917 11.9583 12.1333 12.0749 12.0167C12.1916 11.9 12.2499 11.7833 12.2499 11.6083V9.85833C12.2499 9.56667 12.0166 9.33333 11.7249 9.275C11.1416 9.21667 10.5583 9.04167 9.97494 8.80833C9.7416 8.75 9.50827 8.75 9.33327 8.925L8.57494 9.68333C8.39994 9.85833 8.10827 9.91667 7.87494 9.8C6.29994 8.925 5.0166 7.64167 4.1416 6.06667C4.08327 5.83333 4.1416 5.54167 4.3166 5.36667L5.07494 4.60833C5.1916 4.49167 5.24994 4.2 5.1916 4.025C4.95827 3.44167 4.8416 2.85833 4.72494 2.275C4.72494 1.98333 4.43327 1.75 4.1416 1.75ZM11.0833 5.83333C10.7916 5.83333 10.5583 5.65833 10.4999 5.36667C10.3249 4.43333 9.5666 3.73333 8.63327 3.5C8.3416 3.44167 8.10827 3.15 8.1666 2.8C8.22494 2.50833 8.5166 2.275 8.8666 2.33333C10.2666 2.625 11.3749 3.675 11.6083 5.075C11.6666 5.36667 11.4916 5.71667 11.1416 5.775C11.1416 5.775 11.1416 5.83333 11.0833 5.83333ZM13.4166 5.775C13.1249 5.775 12.8916 5.54167 12.8333 5.25C12.5999 3.09167 10.9083 1.4 8.6916 1.10833C8.39993 1.05 8.1666 0.758333 8.1666 0.466667C8.1666 0.175 8.5166 -0.0583333 8.80827 -0.0583333C11.5499 0.233333 13.6499 2.33333 13.9416 5.075C13.9999 5.36667 13.7666 5.65833 13.4166 5.71667C13.4749 5.775 13.4166 5.775 13.4166 5.775Z" fill="white"/>
                                    </g>
                                    <defs>
                                    <clipPath id="clip0">
                                    <rect width="14" height="14" fill="white"/>
                                    </clipPath>
                                    </defs>
                                </svg>
                                <span class="presentation__number">12100</span>
                            </div>
                        </div>
                        <a class="presentation__link" href="#">View Other Options</a>
                    </div>
                    <div class="presentation__content-map">
                        <googlemap/>
                    </div>
                </div>
            </div>
        </section>
    </div>
</template>
<script>
import PresentationTop from '@/components/PresentationTop'
import Googlemap from './Googlemap.vue'
import TabInfo from '@/components/TabInfo'
export default{
    name: 'Presentation',
    props: {
        currentTab: {
            type: Number,
        },
    },
    components: {
        PresentationTop,
        Googlemap,
        TabInfo
    }
}
</script>
<style lang="scss">
@import '../main.scss';
.presentation{
    &__content{
        border: 1px solid red;
        display: flex;
        justify-content: space-between;
        align-items: center;
    }
    &__content-left{
        max-width: 728px;
        height: 450px;
        display: flex;
        justify-content: center;
        align-items: center;
        margin-right: 30px;
        border-radius: 6px;
        & img {
            width: 100%;
            height: 100%;
        }
    }
    &__content-right{
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        height: 100%;
    }
    &__content-info{
        width: 350px;
        height: 210px;
        margin-bottom: 30px;
        background: #0A223D;
        padding: 26px;
        color: #fff;
        border-radius: 8px;
    }
    &__content-map{
        width: 350px;
        height: 210px;
        border-radius: 8px;
        overflow: hidden;
    }
    &__content-top{
        display: flex;
        justify-content: space-between;
        &--left{
            color: #fff;
        }
        &--bottom{
            display: flex;
            justify-content: space-between;
            margin-top: 19px;
            font-size: 18px;
            margin-bottom: 17px;
        }
    }
    &__icon-box{
        width: 80px;
        display: flex;
        justify-content: space-between;
        align-items: center;
        font-size: 12px;
        &:first-child{
            margin-bottom: 13px;
        }
    }
    &__number{
        font-size: 18px;
    }
    &__link{
        color: #fff;
        text-decoration: none;
        font-size: 14px;
        padding: 13px 84px;
        background: #EC1F46;
        border-radius: 4px;
        display: block;
    }
    
    
}
</style>