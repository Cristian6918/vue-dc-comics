<template>
<div class="main-section">
    <div class="container">
        <div class="left-side">
            <div class="list-part" v-for='{name, listItems } in mainData' :key="name">
                <ul>{{name}}
                     <li v-for="{name,url} in listItems" :key="url"> <a :href='url'>{{name}} </a> </li>
                </ul>
               
                
              
        </div>
    </div>
      <div class="right-side"></div>
</div>
</div>
    
</template>

<script>
import mainData from '@/data/mainData';

export default {
    name:'MainComics',
     data() {
    return {
     mainData,
    };
  },
}
</script>


<style lang="scss" scoped>
.main-section{
    background-image: url('@/img/footer-bg.jpg');
    background-size:cover;
    background-repeat: no-repeat;
    flex-grow:1;
    
  

    .container{
        width: 80%;
        height:100%;
        display: flex;
        margin:auto;

        .right-side{
            background-image: url('@/img/dc-logo-bg.png');
              width: 50%;
            height: 100%;
            background-position: center;
            background-size: 80%;
            background-repeat: no-repeat;
            margin-left:auto;
        }


        .left-side{
            display: flex;
            width:40%;
            padding-top:20px;

            .list-part{
                margin-right:20px;
              
                
                ul{
                    color:white;
                    list-style-type: none;
                    text-align: left;
                    padding-inline-start: 0px;
                    text-transform: capitalize;
                }

                a{
                    text-decoration:none;
                    font-size:0.7rem;
                    color:#787878;
                    text-transform: capitalize;


                }

            }
        }
    
    }
}
</style>