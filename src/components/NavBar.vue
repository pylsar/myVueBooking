<template>
    <div class="container">
        <div class="navbar">
            <div class="navbar__logo">Best<span class="navbar__logo--center"> tour </span>plan</div>
            <div class="navbar__search">
                <input type="text" placeholder="Search Location"/> 
                <button>
                    <svg width="16" height="16" viewBox="0 0 16 16" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <path fill-rule="evenodd" clip-rule="evenodd" d="M7.33325 2.66668C4.75592 2.66668 2.66659 4.75601 2.66659 7.33334C2.66659 9.91067 4.75592 12 7.33325 12C9.91058 12 11.9999 9.91067 11.9999 7.33334C11.9999 4.75601 9.91058 2.66668 7.33325 2.66668ZM1.33325 7.33334C1.33325 4.01963 4.01954 1.33334 7.33325 1.33334C10.647 1.33334 13.3333 4.01963 13.3333 7.33334C13.3333 10.6471 10.647 13.3333 7.33325 13.3333C4.01954 13.3333 1.33325 10.6471 1.33325 7.33334Z" fill="white"/>
                        <path fill-rule="evenodd" clip-rule="evenodd" d="M10.6286 10.6286C10.889 10.3682 11.3111 10.3682 11.5714 10.6286L14.4714 13.5286C14.7318 13.7889 14.7318 14.211 14.4714 14.4714C14.2111 14.7317 13.789 14.7317 13.5286 14.4714L10.6286 11.5714C10.3683 11.311 10.3683 10.8889 10.6286 10.6286Z" fill="white"/>
                    </svg>
                </button>   
            </div>
            <div class="navbar__social">
                <ul>
                    <li>
                        <a href="https://www.codewars.com/users/pylsar" rel="nofollow" target="_blank">
                            <svg class="social-link social-link__one">
                            <use xlink:href="../assets/img/sprite.svg#iconfinder_codewars_4691329"></use>
                            </svg>
                        </a>
                    </li>
                    <li>
                        <a href="https://codepen.io/collection/Aawzba" rel="nofollow" target="_blank">
                            <svg class="social-link social-link__two">
                            <use xlink:href="../assets/img/sprite.svg#iconfinder_Codepen_4550862"></use>
                            </svg>
                        </a>
                    </li>
                    <li>
                        <a href="https://codesandbox.io/u/pylsar" rel="nofollow" target="_blank">
                            <svg class="social-link social-link__three">
                            <use xlink:href="../assets/img/sprite.svg#iconfinder_codesandbox_4691539"></use>
                            </svg>
                        </a>
                    </li>
                    <li>
                        <a href="https://github.com/pylsar" rel="nofollow" target="_blank">
                            <svg class="social-link social-link__four">
                            <use xlink:href="../assets/img/sprite.svg#github"></use>
                            </svg>
                        </a>
                    </li>
                </ul>
            </div>
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
        display: flex;
        justify-content: space-between;
        align-items: center;
        height: 120px;
        &__logo{
            font-size: 24px;
            font-family: 'Luckiest Guy', cursive;
            text-transform: uppercase;
            width: 33%;
            &--center{
                color: #EC1F46;
            }
        }
        &__search{
            width: 33%;
            height: 40px;
            position: relative;
            & input{
                width: 350px;
                height: 100%;
                outline: none;
                border: none;
                border-radius: 6px;
                background: #F5FAFE;
                padding-left: 6px;
            }
            & button {
                position: absolute;
                top: 0;
                right: 0;
                width: 65px;
                height: 40px;
                background: #EC1F46;
                border: none;
                outline: none;
                border-radius: 0px 6px 6px 0px;
            }
        }
        &__social{
            width: 33%;
            & ul{
                list-style: none;
                display: flex;
                justify-content: flex-end;
                align-items: center;
                text-align: right;
                & li{
                    width: 30px;
                    height: 30px;
                    margin-right: 24px;
                    & a {
                        & svg {
                            width: 30px;
                            height: 30px;
                            &:hover{
                                opacity: .8;
                            }
                        }
                    }
                }
            }
        }
    }
</style>