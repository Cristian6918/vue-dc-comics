<template>
    <div class="banner">
        <div class="container">
            <div class="banner-card" v-for="{title,img,alt,id} in bannerData" :key={id}>
                <img :src="img" :alt="alt">
                <a href="">{{title}}</a>
            </div>

        </div>
    </div>
</template>

<script>
import bannerData from '../data/bannerData';

export default{
    name:'BannerComics',
    data() {
    return {
      bannerData,
    };
  },
}

</script>

<style lang="scss" scoped>
.banner{
    width:100%;
    height: 15vh;
    background-color: #0281f7;
    

    .container{
        width:80%;
        height: 100%;
        margin:auto;
        display:flex;
        align-items:center;
        justify-content: space-evenly;

        .banner-card{
            display: flex;
            align-items: center;
            height: 100%;

            img{
                height: 40%;
                
                margin-right:10px;
            }

            a{  
                 text-decoration:none;
                 font-weight: bold;
                text-transform: uppercase;
                color:white;
            }
        }

    }
}
</style>
