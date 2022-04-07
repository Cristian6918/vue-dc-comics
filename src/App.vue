<template>
  <div id="app">
    <HeaderComics/>
    <ComicsMain/>
    <BannerComics/>
    <MainComics/>
    <FooterComics/>
  </div>
</template>

<script>
import HeaderComics from './components/HeaderComics.vue'
import ComicsMain from './components/ComicsMain.vue'
import BannerComics from './components/BannerComics.vue'
import MainComics from './components/MainComics.vue'
import FooterComics from '@/components/FooterComics.vue'

export default {
  name: 'App',
  components: {
    HeaderComics,
    ComicsMain,
    BannerComics,
    MainComics,
    FooterComics,
  }
}
</script>

<style lang="scss">
*{
  margin:0;
  box-sizing: border-box;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  display:flex;
  flex-direction: column;
  height:100vh;
}
</style>
