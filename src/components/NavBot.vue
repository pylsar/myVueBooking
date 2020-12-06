<template>
    <div class="navBot">
        <div class="container">
            <nav class="navbot">
                <ul>
                    <li><a href="#">All Deals</a></li>
                    <li><a href="#">Hotels</a></li>
                    <li><a href="#">Activities</a></li>
                    <li><a href="#">Hotel Day Packages</a></li>
                    <li><a href="#">Restaurants</a></li>
                    <li><a href="#">Events</a></li>
                    <li><a href="#">Rodrigues</a></li>
                </ul>
            </nav>
        </div>
    </div>
</template>
<script>
export default{
    name: 'NavBot',
}
</script>
<style lang="scss">
@import '../main.scss';
.navBot{
    background: #0A223D;
    height: 80px;
}
.navbot{
    & ul {
        display: flex;
        justify-content: space-between;
        align-items: center;
        height: 80px;
        & li {
            list-style: none;
            & a {
                text-decoration: none;
                text-transform: uppercase;
                font-size: 14px;
                color: #FFFFFF;
                &::after{
                    content: '';
                    display: block;
                    width: 0%;
                    height: 1px;
                    background: #fff;
                    transition: all .2s ease-in;
                }
                &:hover {
                    &::after{
                        width: 100%;
                    }
                }
            }
        }
    }
}
</style>