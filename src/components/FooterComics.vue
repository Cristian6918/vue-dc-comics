<template>
  <div class="footer">
      <div class="container">
          <button class="sign-up-button">SIGN-UP NOW!</button>
          <a href="#" class="follow">FOLLOW US</a>
          <a v-for="({name, url} ) in footerData" :key='name'><img :src='url' :alt="name"></a>

      </div>
  </div>
</template>

<script>

import footerData from '@/data/footerData';
export default {
    name:'FooterComics',
     data() {
    return {
     footerData,
    };
  },
}
</script>

<style lang="scss" scoped>
.footer{
    width: 100%;
    height: 10vh;
    background-color:#303030;
   

    .container{
        width:80%;
        height:100%;
        display:flex;
        align-items:center;
        margin:auto;

        button{
           
            margin-right:auto;
            background-color:#303030;
            outline: none;
            border:2px solid #0281f7;
            color:white;
            padding:0.6rem;
            font-size:1.3rem;

            &:active{
                box-shadow:0px 2px 5px 5px#0e5ca5;
            }

        }

        a{
            height:2rem;
            margin-left:1.5rem;


            img{
                height:100%;
            }
        }

        .follow{
            font-size:1.5rem;
            color:#0281f7;
            text-decoration: none;
            
        }
    }

}
</style>