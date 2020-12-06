<template>
    <div class="container">
        <div class="navbar">
            <div class="navbar__logo">Best<span class="navbar__logo--center">tour</span>plan</div>
            <div class="navbar__search">Search</div>
            <div class="navbar__cart">Cart</div>
        </div>
    </div>
    
</template>
<script>
    export default{
        name: 'NavBar',
    }
</script>
<style lang="scss">
    @import '../main.scss';
    .navbar{
        &__logo{
            font-size: 24px;
            font-family: 'Luckiest Guy', cursive;
        }
    }
</style>