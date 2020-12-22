<template>
    <div class="form container">
        <div class="form__left form__item">
            <span>subscribe to our</span>
            <label for="newsletter">Newsletter</label>
            <input type="text" id="newsletter" placeholder="Newsletter">
            <div class="form__btn">
                <button>send</button>
            </div>
        </div>
        <div class="form__right form__item">
            <span>Send us a massege</span>
            <form>
                <div>
                    <input type="text" placeholder="Name">
                    <input type="email" placeholder="Email">
                </div>
                <textarea name="" id="" cols="30" rows="10"></textarea>
                <div class="form__btn">
                    <button>send</button>
                </div>
            </form>
        </div>
    </div>
</template>
<script>
export default {
    name: 'Form'
}
</script>    
<style lang="scss">
.form{
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 100%;
    background: #0A223D;
    &__item{
        padding: 24px;
    }
    & input {
        background: transparent;
        border: none;
        outline: none;
        border-bottom: 1px solid #EC1F46;
        padding-left: 5px;
        font-size: 16px;
        margin-bottom: 12px;
        &::placeholder{
            padding-left: 5px;
            font-size: 16px;
        }
    }
    &__left{
        display: flex;
        flex-direction: column;
        width: 400px;
        height: 400px;
        margin-right: 24px;
        & span {
            display: block;
            margin-bottom: 12px;
            color: #fff;
            font-size: 12px;
        }
        & label {
            font-size: 30px;
            font-weight: 700;
            margin-bottom: 12px;
            color: #fff;
        }
    }
    &__right{
        flex: 1;
        justify-content: center;
        height: 400px;
        & span {
            display: block;
            margin-bottom: 60px;
            color: #fff;
            font-size: 12px;
        }
        & input:first-child{
            margin-right: 24px;
            margin-bottom: 24px;
        }
    }
    &__btn {
        margin-top: auto;
    }
}

</style>