<template>
    <section class="summary" id="options">
        <div class="container">
            <div class="summary__head">
                <h3 class="summary__title">Package Summery</h3>
            </div>
            <div class="summary__box">
                <div class="summary__list">
                    <span class="summary__list-title">Purchase Inclusions</span> 
                    <ul>
                        <li v-for="(purchase,index) in purchases" :key="index">
                            <svg width="16" height="16" viewBox="0 0 16 16" fill="none" xmlns="http://www.w3.org/2000/svg">
                                <path fill-rule="evenodd" clip-rule="evenodd" d="M0.666748 7.99996C0.666748 3.94987 3.94999 0.666626 8.00008 0.666626C12.0502 0.666626 15.3334 3.94987 15.3334 7.99996C15.3334 12.05 12.0502 15.3333 8.00008 15.3333C3.94999 15.3333 0.666748 12.05 0.666748 7.99996Z" fill="#333333"/>
                                <path fill-rule="evenodd" clip-rule="evenodd" d="M11.5405 5.36194C11.8009 5.62229 11.8009 6.0444 11.5405 6.30475L7.40248 10.6381C7.14213 10.8984 6.72002 10.8984 6.45967 10.6381L4.45967 8.63808C4.19932 8.37773 4.19932 7.95562 4.45967 7.69527C4.72002 7.43492 5.14213 7.43492 5.40248 7.69527L6.93107 9.22387L10.5977 5.36194C10.8581 5.10159 11.2802 5.10159 11.5405 5.36194Z" fill="white"/>
                            </svg>  
                            <span>{{purchase.name}}</span> 
                        </li> 
                    </ul>  
                </div>
                <div class="summary__list">
                    <span class="summary__list-title">Complimentary Land Based Activities</span>
                    <ul>
                        <li v-for="(activity,index) in activities" :key="index">
                            <svg width="16" height="16" viewBox="0 0 16 16" fill="none" xmlns="http://www.w3.org/2000/svg">
                                <path fill-rule="evenodd" clip-rule="evenodd" d="M0.666748 7.99996C0.666748 3.94987 3.94999 0.666626 8.00008 0.666626C12.0502 0.666626 15.3334 3.94987 15.3334 7.99996C15.3334 12.05 12.0502 15.3333 8.00008 15.3333C3.94999 15.3333 0.666748 12.05 0.666748 7.99996Z" fill="#333333"/>
                                <path fill-rule="evenodd" clip-rule="evenodd" d="M11.5405 5.36194C11.8009 5.62229 11.8009 6.0444 11.5405 6.30475L7.40248 10.6381C7.14213 10.8984 6.72002 10.8984 6.45967 10.6381L4.45967 8.63808C4.19932 8.37773 4.19932 7.95562 4.45967 7.69527C4.72002 7.43492 5.14213 7.43492 5.40248 7.69527L6.93107 9.22387L10.5977 5.36194C10.8581 5.10159 11.2802 5.10159 11.5405 5.36194Z" fill="white"/>
                            </svg>  
                            <span>{{activity.name}}</span> 
                        </li> 
                    </ul> 
                </div>
                <div class="summary__list">
                    <span class="summary__list-title">Complimentary Water Based Activities</span>
                    <ul>
                        <li v-for="(water,index) in watersports" :key="index">
                            <svg width="16" height="16" viewBox="0 0 16 16" fill="none" xmlns="http://www.w3.org/2000/svg">
                                <path fill-rule="evenodd" clip-rule="evenodd" d="M0.666748 7.99996C0.666748 3.94987 3.94999 0.666626 8.00008 0.666626C12.0502 0.666626 15.3334 3.94987 15.3334 7.99996C15.3334 12.05 12.0502 15.3333 8.00008 15.3333C3.94999 15.3333 0.666748 12.05 0.666748 7.99996Z" fill="#333333"/>
                                <path fill-rule="evenodd" clip-rule="evenodd" d="M11.5405 5.36194C11.8009 5.62229 11.8009 6.0444 11.5405 6.30475L7.40248 10.6381C7.14213 10.8984 6.72002 10.8984 6.45967 10.6381L4.45967 8.63808C4.19932 8.37773 4.19932 7.95562 4.45967 7.69527C4.72002 7.43492 5.14213 7.43492 5.40248 7.69527L6.93107 9.22387L10.5977 5.36194C10.8581 5.10159 11.2802 5.10159 11.5405 5.36194Z" fill="white"/>
                            </svg>  
                            <span>{{water.name}}</span> 
                        </li> 
                    </ul> 
                </div>

            </div>    
        </div>   
    </section>
</template>
<script>
export default{
    name: 'SummaryDetails',
    data(){
        return{
            purchases: [
                {
                    name: 'Room as per selection'
                },
                 {
                    name:  'Half Board or All Inclusive Meal Plan'
                },
                 {
                    name: 'Complimentary Land & Water activities'
                },
                 {
                    name: 'Complimentary Land & Water activities'
                },
                 {
                    name: 'Free Wi-Fi'
                },
            ],
            activities: [
                {
                    name: 'Gym'
                },
                {
                    name: 'Beach Volley'
                },
                {
                    name: 'Table tennis'
                },
                {
                    name: 'Soccer balls'
                },
                {
                    name: 'Yoga'
                },

            ],
            watersports: [
                {
                    name: 'Water skiing'
                },
                {
                    name: 'Windsurfing'
                },
                {
                    name: 'Pedal boats'
                },
                {
                    name: 'Kayaking'
                },
                {
                    name: 'Aqua Gym'
                },
            ]
        }
    }
}
</script>
<style lang="scss">
    .summary{
        padding-bottom: 42px;
        &__head{
            background: #0A223D;
        }
        &__title{
            font-size: 14px;
            font-weight: 700;
            color: #fff;
            padding-top: 16px;
            padding-bottom: 16px;
            padding-left: 24px;
        }
        &__box{
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
        }
        &__list-title{
            display: inline-block;
            margin-top: 24px;
            margin-bottom: 24px;
            color: #EC1F46;
            font-size: 16px;
        }
        &__list{
            & ul{
                & li {
                    list-style: none;
                    margin-top: 12px;
                    display: flex;
                    justify-content: flex-start;
                    align-items: center;
                    font-size: 12px;
                    padding-right: 12px;
                    & svg{
                        margin-right: 24px;
                    }
                }
            }
        }
    }
</style>