<template>
  <div id="app">
    <header>
      <nav-top />
      <nav-bar />
    </header>
    <router-view/>
  </div>
</template>

<script>
import NavTop from '@/components/NavTop.vue';
import NavBar from '@/components/NavBar.vue';
  export default{
    name: 'App',
    components: {
      NavTop,
      NavBar,
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
