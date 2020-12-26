<template>
<div>
    <div class="cart" v-if="cart.length">
        <div v-for="(item, index) in cart" :key="index" class="cart__item">
            <div class="cart__img">
                <img :src=" require('../assets/img/' + item.src) " :alt="item.name">
            </div>
            <div class="cart__content">
                <span>{{item.name}}</span>
                <span>{{item.newprice}}</span>
            </div>
           <div class="cart__btn">
                <button @click="cancel(index)" class="cart__cancel">Отказаться</button>
           </div>
        </div>
    </div>
     <div class="cards">
        <div 
        v-for="(card, index) in cards"
        :key="index" 
        class="card"
        >
            <div class="card__head">
                <img :src=" require('../assets/img/' + card.src) " :alt="card.name">
            </div>
            <div class="card__content">
                <span class="card__name">{{card.name}}</span>
                <p class="card__first">
                   Aute quis duis excepteur excepteur ipsum cat eiusmod consectetur enim laborum magna llit. Ipsum est fugiat velit ea llamco do esse ut in veniam sun in onsequat. Aute quis duis epteur excepteur ipsum occaecat eiusmod nsectetur enim laborum magna mollit. Ipsum est fugiat velit ea ullamco do 
                </p>
                <div class="card__info">
                    <div class="card__info-item">
                        <svg width="14" height="14" viewBox="0 0 14 14" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <path fill-rule="evenodd" clip-rule="evenodd" d="M7.00008 1.16667C5.7624 1.16667 4.57542 1.65833 3.70025 2.5335C2.82508 3.40867 2.33341 4.59566 2.33341 5.83333C2.33341 7.64053 3.50926 9.39415 4.79855 10.7551C5.43127 11.4229 6.06597 11.9697 6.54314 12.3497C6.72073 12.4911 6.87584 12.6089 7.00008 12.7007C7.12432 12.6089 7.27943 12.4911 7.45702 12.3497C7.93419 11.9697 8.56889 11.4229 9.20161 10.7551C10.4909 9.39415 11.6667 7.64053 11.6667 5.83333C11.6667 4.59566 11.1751 3.40867 10.2999 2.5335C9.42474 1.65833 8.23776 1.16667 7.00008 1.16667ZM7.00008 13.4167C6.67651 13.902 6.67636 13.9019 6.67619 13.9018L6.67452 13.9007L6.67064 13.8981L6.65727 13.8891C6.64591 13.8813 6.62971 13.8703 6.60899 13.8559C6.56756 13.8272 6.50802 13.7854 6.43296 13.7312C6.2829 13.6228 6.07046 13.4646 5.8164 13.2623C5.30919 12.8584 4.63139 12.275 3.95161 11.5574C2.6159 10.1475 1.16675 8.10947 1.16675 5.83333C1.16675 4.28624 1.78133 2.80251 2.87529 1.70854C3.96925 0.614581 5.45299 0 7.00008 0C8.54718 0 10.0309 0.614581 11.1249 1.70854C12.2188 2.80251 12.8334 4.28624 12.8334 5.83333C12.8334 8.10947 11.3843 10.1475 10.0486 11.5574C9.36877 12.275 8.69097 12.8584 8.18377 13.2623C7.9297 13.4646 7.71726 13.6228 7.5672 13.7312C7.49214 13.7854 7.43261 13.8272 7.39117 13.8559C7.37045 13.8703 7.35425 13.8813 7.3429 13.8891L7.32953 13.8981L7.32564 13.9007L7.32441 13.9015C7.32424 13.9016 7.32366 13.902 7.00008 13.4167ZM7.00008 13.4167L7.32366 13.902C7.12772 14.0327 6.87213 14.0324 6.67619 13.9018L7.00008 13.4167Z" fill="white"/>
                            <path fill-rule="evenodd" clip-rule="evenodd" d="M7.00008 4.66667C6.35575 4.66667 5.83341 5.189 5.83341 5.83333C5.83341 6.47767 6.35575 7 7.00008 7C7.64441 7 8.16675 6.47767 8.16675 5.83333C8.16675 5.189 7.64441 4.66667 7.00008 4.66667ZM4.66675 5.83333C4.66675 4.54467 5.71142 3.5 7.00008 3.5C8.28875 3.5 9.33342 4.54467 9.33342 5.83333C9.33342 7.122 8.28875 8.16667 7.00008 8.16667C5.71142 8.16667 4.66675 7.122 4.66675 5.83333Z" fill="white"/>
                        </svg>
                        <span>{{card.adress}}</span>
                    </div>
                    <div class="card__info-item">
                        <svg width="14" height="14" viewBox="0 0 14 14" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <path fill-rule="evenodd" clip-rule="evenodd" d="M2.60427 9.02094C3.15125 8.47396 3.89312 8.16666 4.66667 8.16666H9.33333C10.1069 8.16666 10.8487 8.47396 11.3957 9.02094C11.9427 9.56792 12.25 10.3098 12.25 11.0833V12.25C12.25 12.5722 11.9888 12.8333 11.6667 12.8333C11.3445 12.8333 11.0833 12.5722 11.0833 12.25V11.0833C11.0833 10.6192 10.899 10.1741 10.5708 9.84589C10.2426 9.51771 9.79746 9.33333 9.33333 9.33333H4.66667C4.20254 9.33333 3.75742 9.51771 3.42923 9.84589C3.10104 10.1741 2.91667 10.6192 2.91667 11.0833V12.25C2.91667 12.5722 2.6555 12.8333 2.33333 12.8333C2.01117 12.8333 1.75 12.5722 1.75 12.25V11.0833C1.75 10.3098 2.05729 9.56792 2.60427 9.02094Z" fill="white"/>
                            <path fill-rule="evenodd" clip-rule="evenodd" d="M6.99992 2.33333C6.03342 2.33333 5.24992 3.11683 5.24992 4.08333C5.24992 5.04983 6.03342 5.83333 6.99992 5.83333C7.96642 5.83333 8.74992 5.04983 8.74992 4.08333C8.74992 3.11683 7.96642 2.33333 6.99992 2.33333ZM4.08325 4.08333C4.08325 2.4725 5.38909 1.16666 6.99992 1.16666C8.61075 1.16666 9.91659 2.4725 9.91659 4.08333C9.91659 5.69416 8.61075 7 6.99992 7C5.38909 7 4.08325 5.69416 4.08325 4.08333Z" fill="white"/>
                        </svg>
                        <span>{{card.guests}} x Guests</span>
                    </div>
                    <div class="card__info-item">
                        <svg width="14" height="14" viewBox="0 0 14 14" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <path fill-rule="evenodd" clip-rule="evenodd" d="M6.64195 0.70621C6.8526 0.542373 7.14757 0.542373 7.35821 0.70621L12.6082 4.78954C12.7503 4.90006 12.8334 5.06999 12.8334 5.25V11.6667C12.8334 12.1308 12.649 12.5759 12.3209 12.9041C11.9927 13.2323 11.5475 13.4167 11.0834 13.4167H2.91675C2.45262 13.4167 2.0075 13.2323 1.67931 12.9041C1.35112 12.5759 1.16675 12.1308 1.16675 11.6667V5.25C1.16675 5.06999 1.24986 4.90006 1.39195 4.78954L6.64195 0.70621ZM2.33341 5.5353V11.6667C2.33341 11.8214 2.39487 11.9697 2.50427 12.0791C2.61367 12.1885 2.76204 12.25 2.91675 12.25H11.0834C11.2381 12.25 11.3865 12.1885 11.4959 12.0791C11.6053 11.9697 11.6667 11.8214 11.6667 11.6667V5.5353L7.00008 1.90567L2.33341 5.5353Z" fill="white"/>
                            <path fill-rule="evenodd" clip-rule="evenodd" d="M4.66675 7C4.66675 6.67783 4.92792 6.41667 5.25008 6.41667H8.75008C9.07225 6.41667 9.33342 6.67783 9.33342 7V12.8333C9.33342 13.1555 9.07225 13.4167 8.75008 13.4167C8.42792 13.4167 8.16675 13.1555 8.16675 12.8333V7.58333H5.83342V12.8333C5.83342 13.1555 5.57225 13.4167 5.25008 13.4167C4.92792 13.4167 4.66675 13.1555 4.66675 12.8333V7Z" fill="white"/>
                        </svg>
                        <span>{{card.rooms}} x Room</span>
                    </div>
                </div>
                <span class="card__old-price">{{card.oldprice}}</span>
                <div class="card__buy">
                    <span class="card__price">{{card.newprice}}</span>
                    <a 
                    @click="addToCart(card)"
                    href="#"
                    :class="{ 'isBlocked' : disabled}"
                    >Book Now</a>
                </div>
            </div>
        </div>
    </div>    
</div>
   
</template>
<script>
export default{
    name: 'Card',
    data(){
        return{
            cards: [
                {
                    name: 'Hotel Blue Haven',
                    src: '2.png',
                    oldprice: '$ 10,500',
                    newprice: '$ 8,500',
                    adress: '1th street pasadena',
                    guests: 2,
                    rooms: 2
                },
                {
                    name: 'LUX* Belle Mare',
                    src: '3.png',
                    oldprice: '$ 8,500',
                    newprice: '$ 3,000',
                    adress: '3th street brodway',
                    guests: 3,
                    rooms: 2
                },
                {
                    name: 'White Palace',
                    src: '4.png',
                    oldprice: '$ 10,500',
                    newprice: '$ 9,500',
                    adress: '17th street luisiana',
                    guests: 2,
                    rooms: 1
                },
                {
                    name: 'Luxury Place',
                    src: '5.png',
                    oldprice: '$ 4,500',
                    newprice: '$ 2,500',
                    adress: 'new street NY',
                    guests: 1,
                    rooms: 1
                },
                 {
                    name: 'Hotel Five Star',
                    src: '6.png',
                    oldprice: '$ 6,500',
                    newprice: '$ 3,500',
                    adress: 'old street LA',
                    guests: 2,
                    rooms: 2
                },
            ],
            cart:[],
            disabled: false
        }
    },
    methods:{
        addToCart(card){
            this.cart.push(card);
            this.disabled = true;
            // console.log(this.cart)
        },
        cancel(index){
            this.cart.splice(index,1);
            this.disabled = false;
        }
    }
}
</script>
<style lang="scss">
.cart{
    position: fixed;
    top: 0;
    left:0;
    right: 0;
    z-index: 1000;
    min-height: 100px;
    background: lighten(#0A223D, 5%);
    &__item {
        width: 100%;
        height: 100px;
        display: flex;
        justify-content: space-around;
        align-items: center;
    }
    &__img{
        width: 80px;
        height: 80px;
        box-shadow: 10px 5px 5px black;
        border-radius: 6px;
        & img {
            width: 100%;
            height: 100%;
        }
    }
    &__content{
        display: flex;
        flex-direction: column;
        color: #fff;
    }
    &__btn{
        display: flex;
    }
    &__cancel{
        background: #EC1F46;
        color: #fff;
        font-size: 14px;
        padding: 11px 26px;
        border-radius: 6px;
        outline: none;
        border: none;
        cursor: pointer;
        &:hover{
            opacity: .8;
        }
    }
}
.cards{
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
}
.card{
    width: 350px;
    height: 500px;
    border-radius: 6px;
    background: #0A223D;
    margin-right: 16px;
    margin-bottom: 24px;
    &:nth-child(2){
        margin-right: 0;
    }
    &__head{
        height: 50%;
        border-radius: 6px 6px 0px 0px;
        & img{
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
    }
    &__content{
        padding: 30px;
        border-radius: 0px 0px 6px 6px;
        color: #fff;
    }
    &__name{
        font-size: 18px;
        font-weight: 700;
        display: block;
        margin-bottom: 24px;
    }
    &__info{
        display: flex;
        flex-direction: column;
        font-size: 12px;
        & svg{
            margin-right: 14px;
        }
    }
    &__info-item{
        margin-bottom: 12px;
    }
    &__old-price{
        margin-top: 24px;
        text-decoration: line-through;
        font-size: 14px;
    }
    &__price{
        font-size: 24px;
        font-weight: 700;
    }
    &__buy{
        display: flex;
        justify-content: space-between;
        align-items: center;
        & a {
            background: #EC1F46;
            text-decoration: none;
            color: #fff;
            font-size: 14px;
            padding: 11px 26px;
            border-radius: 6px;
            &:hover{
                opacity: .8;
            }
        }
    }
    
    &:last-child{
        margin-right: 0;
    }
    &__first{
        display: none;
    }
    &:first-child{
        width: 730px;
        display: flex;
        & .card__first{
            display: block;
        }
        & .card__head{
            height: 100%;
            & img {
                height: 100%;
            }
        }
        & .card__head, .card__content{
            width: 50%;
        }
        & .card__info{
            margin-top: 86px;
        }

    }
}
.isBlocked{
    background: gray!important;
    pointer-events: none;
}

@media screen and (max-width: 1166px) {
    .card{
        width: calc(50% - 12px);
        margin-right: 0;
        &:first-child{
            width: 100%;
        }
        &__head{
            height: 250px;
            & img{
                border-radius: 6px 6px 0px 0px;
            }
        }
    }
}

@media screen and (max-width: 768px) {
    .card{
        &:first-child{
           & .card__info{
               margin-top: 40px;
           } 
        }
    }
}

@media screen and (max-width: 640px) {
    .card{
        width: 100%;
        &:first-child{
            flex-direction: column;
            & .card__head{
                width: 100%;
                height: 250px;
                & img{
                    border-radius: 6px 6px 0px 0px;
                }
            }
            & .card__first{
                display: none;
            }
            & .card__content{
                width: 100%;
            }
            & .card__info{
                margin-top: 0;  
            }
        }
    }
}

</style>