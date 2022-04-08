<template>
  <div id="app">
    <HeaderComics/>
    <ComicsMain :cardData="cardInfo"/>
    <BannerComics />
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
import cardInfo from '@/data/dc-comics.json'

export default {
  name: 'App',
  components: {
    HeaderComics,
    ComicsMain,
    BannerComics,
    MainComics,
    FooterComics,
  },
  data(){
    return{
      cardInfo,
    };
  }
};
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
  
}
</style>
