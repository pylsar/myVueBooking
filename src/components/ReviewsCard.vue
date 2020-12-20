<template>
    <div>
        <div
            @click="left" 
            class="reviews-card__arrow-left"
        >
            <svg width="30" height="30" viewBox="0 0 30 30" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path fill-rule="evenodd" clip-rule="evenodd" d="M19.6339 6.61612C20.122 7.10427 20.122 7.89573 19.6339 8.38388L13.0178 15L19.6339 21.6161C20.122 22.1043 20.122 22.8957 19.6339 23.3839C19.1457 23.872 18.3543 23.872 17.8661 23.3839L10.3661 15.8839C9.87796 15.3957 9.87796 14.6043 10.3661 14.1161L17.8661 6.61612C18.3543 6.12796 19.1457 6.12796 19.6339 6.61612Z" fill="#828282"/>
            </svg>
        </div>
        <div class="reviews-card__body" :style="{ 'margin-left': '-' + 100 * currentSlide + '%' }">
            <div
                v-for="(review, index) in reviews" 
                :key="index"
                class="reviews-card"
            >
                <div class="reviews-card__head">
                    <div class="reviews-card__img">
                        <img :src=" require('../assets/img/' + review.src) " :alt="review.name">
                    </div>
                    <span class="reviews-card__percone">{{review.name}}</span>
                    <time class="reviews-card__date">{{review.day}}</time>
                    <div class="reviews-card__stars">
                        <span>&#9733;</span>
                        <span>&#9733;</span>
                        <span>&#9733;</span>
                        <span>&#9733;</span>
                        <span>&#9733;</span>
                    </div>
                </div>
                <div class="reviews-card__content">
                    <p>It was very nice hotel with cleanliness. Staff behavior was good and polite. They welcome us very well. Issue was only that Lift was not in working and we were allotted to 3rd floor and amenities articles were in corner of gallery which were giving bad feeling. Breakfast was good and support of the staff was also very nice. Location is not good as per atmosphere, it is very nearby most of the popular places but self location in a narrow street is not good. Overall it was a good experience and could recommend. </p>
                </div>
            </div>

            
        </div>
        <div 
            @click="right"
            class="reviews-card__arrow-right"
        >
            <svg width="30" height="30" viewBox="0 0 30 30" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path fill-rule="evenodd" clip-rule="evenodd" d="M19.6339 6.61612C20.122 7.10427 20.122 7.89573 19.6339 8.38388L13.0178 15L19.6339 21.6161C20.122 22.1043 20.122 22.8957 19.6339 23.3839C19.1457 23.872 18.3543 23.872 17.8661 23.3839L10.3661 15.8839C9.87796 15.3957 9.87796 14.6043 10.3661 14.1161L17.8661 6.61612C18.3543 6.12796 19.1457 6.12796 19.6339 6.61612Z" fill="#828282"/>
            </svg>
        </div>
    </div>
</template>
<script>
export default {
    name: 'ReviewsCard',
    data(){
        return{
            currentSlide: 0,
            reviews: [
                {
                    src: 'face1.png',
                    name: 'Megan Fox',
                    day: 'Stayed 18 Nov, 2019',
                },
                {
                    src: 'face2.jpg',
                    name: 'Dalay Lama',
                    day: 'Stayed 01 Sep, 2019',
                },
                {
                    src: 'face3.jpg',
                    name: 'Stifen King',
                    day: 'Stayed 31 Dec, 2019',
                }
            ]
        }
    },
    methods: {
    left() {
      if (this.currentSlide <= 0) {
        this.currentSlide = this.reviews.length - 1;
      } else {
        this.currentSlide--;
      }
    },
    right() {
      if (this.currentSlide >= this.reviews.length - 1) {
        this.currentSlide = 0;
      } else {
        this.currentSlide++;
      }
    },
  },
}
</script>  
<style lang="scss">
.reviews-card{
    min-width: 100%;
    width: 100%;
    height: 400px;
    margin: 0 auto;
    display: flex;
    flex-direction: column;
    align-items: center;
    &__body{
        display: flex;
        min-width: 100%;
        width: 100%;
    }
    &__head{
        width: 200px;
        height: auto;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }
    &__content{
        max-width: 100%;
        padding: 24px;
    }
    &__img{
        margin-bottom: 10px;
        width: 90px;
        height: 90px;
        border-radius: 50%;
        overflow: hidden;
        & img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
    }
    &__percone{
        color: #EC1F46;
        font-size: 12px;
        font-weight: bold;
        margin-bottom: 10px;
    }
    &__date{
        margin-bottom: 10px;
    }
    &__stars{
        color: #F2994A;
    }
    &__arrow-left, &__arrow-right{
        position: absolute;
        top: 50%;
        cursor: pointer;
    }
    &__arrow-left{
        left: 10%;
    }
    &__arrow-right{
        right: 10%;
        transform: rotate(180deg);
    }
}
</style>