<template>
  <div id="app">
    <header>
      <nav-top />
      <nav-bar />
      <nav-bot />
    </header>
    <main>
      <presentation />
    </main>
    <router-view/>
  </div>
</template>

<script>
import NavTop from '@/components/NavTop.vue';
import NavBar from '@/components/NavBar.vue';
import NavBot from '@/components/NavBot.vue';
import Presentation from '@/components/Presentation.vue';
  export default{
    name: 'App',
    components: {
      NavTop,
      NavBar,
      NavBot,
      Presentation
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
