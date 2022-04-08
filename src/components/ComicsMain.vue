<template>
<div class="main-container">
    <div class="jumbtron"> 
        <div class="series-label">CURRENT SERIES</div>
         </div>
   
    <div class="film-container">
         
            <div clasS='container'>
                
                <FilmCard v-for='{thumb ,price, series, type} in cardData' :key='series+price+type'
                :thumb="thumb"
                :price="price"
                :series="series"
                :type="type"
                />
                
        
            </div>
            <button>Load More</button>
        </div>
</div>
</template>

<script>

import FilmCard from '@/components/FilmCard.vue';
export default {
    name:'ComicsMain',
    components:{FilmCard},
    props:["cardData"],
    };
</script>

<style lang="scss" scoped>



.jumbtron{
    width:100%;
    background-image:url('../img/jumbotron.jpg');
    height:40vh;
    background-size: cover;
       position:relative;
}



.series-label{
    height:4vh;
    font-size:1.2rem;
    width:15%;
    position:absolute;
    left:10%;
    bottom:-2vh;
    background-color:#0281f7;
    color:white;
    padding:10px;

}

.film-container{
    width:100%;
    background-color:#1C1C1C;
    padding:3em;
  

    .container{
        width:80%;
        margin:auto;
        display: flex;
        justify-content: space-between;
        flex-wrap: wrap;
       
       
        

    }
   }
   button{
       margin:2rem;
       border:none;
       font-size:1.5rem;
       font-weight: bold;
       background-color: #0281f7;
       color:white;
       padding:10px 30px;
       cursor:pointer;
   
   &:active{
        box-shadow:0px 2px 5px 5px#0e5ca5;
   }
   }
</style>




