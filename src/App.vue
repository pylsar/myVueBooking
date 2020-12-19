<template>
  <div id="app">
    <header>
      <nav-top />
      <nav-bar />
      <nav-bot />
    </header>
    <main>
      <presentation :currentTab="currentTab"/>
      <tabs 
        @tabClickSum = "tabClickSum"
        @tabClickMeal = "tabClickMeal"
        @tabClickEx = "tabClickEx"
        @tabClickTr = "tabClickTr"
      />
      <summary-details /> 
      <package />
      <reviews />
    </main>
    <div style="margin-top: 100px;"></div>
  </div>
</template>

<script>
import NavTop from '@/components/NavTop.vue';
import NavBar from '@/components/NavBar.vue';
import NavBot from '@/components/NavBot.vue';
import Presentation from '@/components/Presentation.vue';
import Tabs from '@/components/Tabs.vue'
import SummaryDetails from './components/SummaryDetails.vue';
import Package from './components/Package.vue';
import Reviews from './components/Reviews.vue';
  export default{
    name: 'App',
    components: {
      NavTop,
      NavBar,
      NavBot,
      Presentation,
      Tabs,
      SummaryDetails,
      Package,
      Reviews,
    },
    data(){
      return{
      currentTab: 0
      }
    },
    methods:{
      tabClickSum(){
          this.currentTab = 0;
      },
      tabClickMeal(){
          this.currentTab = 1;
      },
      tabClickEx(){
          this.currentTab = 2;
      },
      tabClickTr(){
          this.currentTab = 3;
      }
    }
  }
</script>

<style lang="scss">
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
body{
  background: #fff;
}
#app {
  // font-family: 'Luckiest Guy', cursive;
  font-family: 'Mulish', sans-serif;
}


</style>
