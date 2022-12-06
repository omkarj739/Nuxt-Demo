<template>
    <section class="first_section">
       <h1 class="title"> HEALTH PLAN</h1>
       <div v-for="item in items" class="heal">
            <div  class="heal_left">
                <h2>{{item.title}}</h2>
                <ul>
                    <li>{{item.description}}</li>
                    <li>{{item.description}}</li>
                    <li>{{item.description}}</li>
                </ul>
            </div>
            <div class="heal_addd">
                <img src="../images/heal_addd.png" alt="img" >
            </div>
            <div class="heal_right">
            </div>
       </div>
       <!-- <div class="heal">
        <div class="heal_right"></div>
        <div class="heal_addd">
            <img src="../images/heal_addd.png" alt="img" >
        </div>
         <div class="heal_left">
            <h2>engage</h2>
            <ul>
                <li>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Lorem ipsum dolor sit amet, consectetur adipiscing elit.</li>
                <li>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Lorem ipsum dolor sit amet, consectetur adipiscing elit.</li>
                <li>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Lorem ipsum dolor sit amet, consectetur adipiscing elit.</li>
            </ul>
        </div>
       </div>
       <div class="heal">
         <div class="heal_left">
            <h2>engage</h2>
            <ul>
                <li>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Lorem ipsum dolor sit amet, consectetur adipiscing elit.</li>
                <li>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Lorem ipsum dolor sit amet, consectetur adipiscing elit.</li>
                <li>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Lorem ipsum dolor sit amet, consectetur adipiscing elit.</li>
            </ul>
        </div>
        <div class="heal_addd">
            <img src="../images/heal_addd.png" alt="img" >
        </div>
        <div class="heal_right"></div>
       </div> -->
    </section>
</template>

<script>
export default {
  name: 'section_6',
  data(){
      return{
          items:[
              {
                  title:'heal',
                  description:'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Lorem ipsum dolor sit amet, consectetur adipiscing elit.'
              },
              {
                  title:'ENGAGE',
                  description:'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Lorem ipsum dolor sit amet, consectetur adipiscing elit.'
              },
              {
                  title:'STAY FIT',
                  description:'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Lorem ipsum dolor sit amet, consectetur adipiscing elit.'
              }
          ]
      }
  }
}
</script>
<style scoped>
    .first_section{
        display: flex;
        flex-direction: column;
        text-align: center;
    }
    .first_section .heal{
        display: flex;
        justify-content: center;
    }
    .first_section .heal:nth-child(2){
        flex-direction: row-reverse;
    }
    .first_section .heal:nth-child(4){
        flex-direction: row-reverse;
    }
    .first_section h1.title{
        text-transform: uppercase;
        font-weight: 700;
        color: #000;
        padding:20px 0;
        font-size: 25px !important;
    }
    .first_section .heal .heal_left{
        display: flex;
        flex-direction: column;
        text-align: left;
        background: #284948;
        width: 50%;
        padding: 40px;
    }
    .first_section .heal .heal_left h2{
        text-transform: uppercase;
        font-weight: 700;
        color: #C3D797;
        margin-bottom: 20px;
    }
    .first_section .heal .heal_left ul li{
        color: #FFFFFF;
        margin-bottom: 10px;
    }
    .first_section .heal .heal_addd img{
        object-fit: cover;
        position: absolute;
        width: 100px;
        height:100px;
        margin: 100px 0 0 -50px ;
        background-color: white;
        border-radius: 100%;
        padding: 10px;
    }
    .first_section .heal .heal_right{
        background: #284948;
        width: 50%;
        background-image: url('../images/heal_1.png');
        background-position: center;
        background-size: cover;
        background-repeat: no-repeat;
    }
     @media screen and (min-width:300px) and (max-width:500px) {
         .first_section .heal{
             flex-direction: column;
         }  
         .first_section .heal .heal_left{
             width: 100%;
         } 
         .first_section .heal .heal_right{
             width: 100%; 
            height: 300px;
         } 
         .first_section .heal .heal_addd{
             display: none;
         }
         .first_section .heal:nth-child(2){
             flex-direction: column-reverse;
         }
         .first_section .heal:nth-child(4){
            flex-direction: column;
        }
     }
      @media screen and (min-width:501px) and (max-width:768px) {
         .first_section .heal{
             flex-direction: column;
         }  
         .first_section .heal .heal_left{
             width: 100%;
         } 
         .first_section .heal .heal_right{
             width: 100%; 
            height: 300px;
         } 
         .first_section .heal .heal_addd{
             display: none;
         }
         .first_section .heal:nth-child(2){
             flex-direction: column-reverse;
         }
         .first_section .heal:nth-child(4){
            flex-direction: column;
        }
     }
</style>
