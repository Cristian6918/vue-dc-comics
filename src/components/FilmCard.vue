<template>
    <div class='film-card'>
        <div class="image-container">
            <img class="film-img" :src="thumb" :alt='series + type + price'>

        </div>
        <div class="title-container">{{series}}</div>
        
    </div>

  
</template>

<script>

export default {
    name:'FilmCard',
    props:{
        thumb:String,
        price:String,
        series:String,
        type:String
    }

};
</script>

<style lang="scss" scoped>
.film-card{
    width:calc(100% /6 - 20px);
    margin:1rem 0;
    color:white;
    text-align: left;
    cursor:pointer;
    transition:transform 0.5s;

    
     &:hover {
           transform:scale(1.3);
           z-index:1;
           

        
        }

      


    .image-container{
        width:100%;
        aspect-ratio:1;
        position:relative;
        overflow: hidden;

       
       
       

          .film-img{
            width:100%;
            position: absolute;
            top:0;
            left:0;
      
            
        }
         
    }
    }

    
   
        
        

      


    .title-container{
      margin-top:1rem; 
      
    }

</style>