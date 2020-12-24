<template>
    <div class="form container">
        <div class="form__left form__item">
            <span>Subscribe to our</span>
            <label for="newsletter">Newsletter</label>
            <input type="text" id="newsletter" placeholder="Newsletter">
            <div class="form__btn">
                <button>send</button>
            </div>
        </div>
        <div class="form__right form__item">
            <span>Send us a massege</span>
            <form>
                <div class="form__field">
                    <input type="text" placeholder="Name">
                    <input type="email" placeholder="Email">
                </div>
                <div class="form__area-wrap">
                    <textarea maxlength="300"></textarea>
                </div>
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
        padding-bottom: 5px;
        font-size: 16px;
        margin-bottom: 12px;
        &::placeholder{
            padding-left: 5px;
            padding-bottom: 5px;
            font-size: 16px;
        }
    }
    &__left{
        display: flex;
        flex-direction: column;
        width: 50%;
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
        width: 50%;
        height: 400px;
        display: flex;
        flex-direction: column;
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
        & textarea {
            background: transparent;
            width: 100%;
            max-height: 150px;
            height: 100%;
            border: 1px solid #EC1F46;
            resize: none;
            padding: 5px;
            color: #fff;
            border-radius: 6px;
            &:focus{
                outline: none;
            }
        }
    }
    &__area-wrap{
        width: 87%;
        height: 55%;
        margin-bottom: 36px;
    }
    &__btn {
        margin-top: auto;
        & button {
            background: #EC1F46;
            color: #fff;
            font-size: 14px;
            padding: 11px 26px;
            border-radius: 6px;
            border: none;
            outline: none;
        }
    }
    &__field{
        height: 90px;
    }
}

</style>