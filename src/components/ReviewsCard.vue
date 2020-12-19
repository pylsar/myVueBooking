<template>
    <div class="reviews-card">
        <div class="reviews-card__head">
            <div class="reviews-card__img">
                <img src="" alt="">
            </div>
            <span>Megan Fox</span>
            <time>Stayed 18 Nov, 2019</time>
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
</template>
<script>
export default {
    name: 'ReviewsCard',
}
</script>  
<style lang="scss">
.reviews-card{
    max-width: 730px;
    height: 354px;
    margin: 0 auto;
    -webkit-box-shadow: 0 0 10px rgba(0,0,0,0.5);
    -moz-box-shadow:    0 0 10px rgba(0,0,0,0.5);
    box-shadow:         0 0 10px rgba(0,0,0,0.5);
    display: flex;
    flex-direction: column;
    align-items: center;
    &__head{
        width: 100px;
        height: 150px;
        border: 1px solid red;

    }
    &__content{
        flex: 1;
        border: 1px solid green;
    }
}
</style>