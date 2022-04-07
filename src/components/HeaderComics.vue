<template>
    <div class="ct-header">
        <div class="container">
            <img src="../img/dc-logo.png" alt="">
            <div class='ct-link' v-for="{ title, id } in headerData" :key={id} >
                 <a href="">{{title}}</a>
            </div>
           

        </div>
    </div>
</template>

<script>
import headerData from '../data/headerData';

export default {
 name:'HeaderComics',
  data() {
    return {
      headerData,
    };
  },

}
</script>



<style lang="scss" scoped>

.ct-header{
    width:100%;
    height:15vh;
  


    .container{
        height: 100%;
        width:80%;
        display:flex;
        align-items:center;
        margin:auto;

        img{
            height: 80%;
            margin-right: auto;
        }

        .ct-link{
            height: 100%;
            display:flex;
            align-items:center;
            height:100%;
            margin-right:1rem;
            

            a{
                 text-decoration:none;
                font-weight: bold;
                text-transform: uppercase;
                color:black;
            }
        }

        .ct-link:hover {
            box-shadow: 0px -5px #0281f7 inset;

            a{
                color:#0281f7;
            }
        }


    }

}

</style>
