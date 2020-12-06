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
            <div class="navbar__cart">
                <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <g clip-path="url(#clip0)">
                    <path fill-rule="evenodd" clip-rule="evenodd" d="M7 21C7 19.8954 7.89543 19 9 19C10.1046 19 11 19.8954 11 21C11 22.1046 10.1046 23 9 23C7.89543 23 7 22.1046 7 21Z" fill="black"/>
                    <path fill-rule="evenodd" clip-rule="evenodd" d="M18 21C18 19.8954 18.8954 19 20 19C21.1046 19 22 19.8954 22 21C22 22.1046 21.1046 23 20 23C18.8954 23 18 22.1046 18 21Z" fill="black"/>
                    <path fill-rule="evenodd" clip-rule="evenodd" d="M0 1C0 0.447715 0.447715 0 1 0H5C5.47663 0 5.88701 0.336385 5.98055 0.803743L6.82043 5H23C23.298 5 23.5805 5.13293 23.7705 5.36256C23.9605 5.59218 24.0381 5.89458 23.9823 6.18733L22.3809 14.5848C22.2437 15.2754 21.868 15.8958 21.3195 16.3373C20.7738 16.7766 20.0916 17.011 19.3914 17H9.68864C8.98837 17.011 8.3062 16.7766 7.76048 16.3373C7.21225 15.8959 6.83664 15.2759 6.69933 14.5857C6.69927 14.5854 6.69939 14.5859 6.69933 14.5857L5.02879 6.2392C5.02201 6.21159 5.01638 6.18353 5.01195 6.15508L4.18032 2H1C0.447715 2 0 1.55228 0 1ZM7.22073 7L8.66084 14.1952C8.70656 14.4254 8.83179 14.6322 9.01461 14.7793C9.19743 14.9265 9.42619 15.0047 9.66084 15.0002L9.68 15H19.4L19.4192 15.0002C19.6538 15.0047 19.8826 14.9265 20.0654 14.7793C20.2474 14.6328 20.3723 14.4273 20.4185 14.1984L21.7913 7H7.22073Z" fill="black"/>
                    </g>
                    <defs>
                    <clipPath id="clip0">
                    <rect width="24" height="24" fill="white"/>
                    </clipPath>
                    </defs>
                </svg>
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
        &__cart{
            width: 33%;
            text-align: right;
            & svg{
                width: 32px;
                height: 32px;
            }
        }
    }
</style>