<template>
    <footer class="footer container">
        <div class="footer__form">
            <div class="footer__left">
                <label for="newsletter"></label>
                <input type="text" id="newsletter">
                <button>send</button>
            </div>
            <div class="footer__right">
                <span>Send us a massege</span>
                <form>
                    <div>
                        <input type="text">
                        <input type="password">
                    </div>
                    <textarea name="" id="" cols="30" rows="10"></textarea>
                    <button>send</button>
                </form>
            </div>
        </div>
        <div class="footer__copy">
            Disclaimer    Conditions of use    Cancellation policy
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