<template>
    <footer class="footer container">

        <div class="footer__copy">
            Lorem ipsum dolor sit amet consectetur, adipisicing elit.
        </div>
    </footer>
</template>

<script>
export default{
    name: 'TheFooter',

}
</script>  
<style lang="scss">
    .footer{
        height: 540px;
        background-size: cover;
        background-repeat: no-repeat;
        background-position: 50% 50%;
        background-image: url('../assets/img/footer.jpg');
        position: fixed;
        bottom: 0;
        left: 0;
        right: 0;
        z-index: -1;
    }
</style>