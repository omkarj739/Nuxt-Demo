<template>
    <section class="first_section">
       <div class="left_div">
           <h2>HOLISTIC WELLNESS:</h2>
           <h4>NATURAL THERAPIES IDENTIFY THE ROOT CAUSE</h4>
           <ul>
               <li>
                   Lorem ipsum dolor sit amet, consectetur adipiscing elit. Lorem ipsum dolor sit amet, consectetur adipiscing elit.Lorem ipsum dolor sit amet, consectetur adipiscing elit.
               </li>
               <li>
                   Lorem ipsum dolor sit amet, consectetur adipiscing elit. Lorem ipsum dolor sit amet, consectetur adipiscing elit.Lorem ipsum dolor sit amet, consectetur adipiscing elit.
               </li>
           </ul>
       </div>
       <div class="right_div">
           <h2>6 DIMENSIONS OF WELLNESS</h2>
            <div class="boxes">
                <div v-for="item in items" class="box">
                    <div class="box_inner">
                        <img src="../images/dimension_icon_1.png" alt="img">
                    </div>
                    <p>{{item.titles}}</p>
                </div>
            </div>
       </div>
    </section>
</template>

<script>
export default {
  name: 'section_5',
  data(){
      return{
          items:[
              {titles:'Ayurveda'},
              {titles:'Homeopathy'},
              {titles:'Yoga'},
              {titles:'Naturopathy'},
              {titles:'Meditation'},
              {titles:'Physiotherapy'}
          ]
      }
  }
}
</script>
<style scoped>
    h1,h2,h3,h4,h5,li,p{
        color: #284948;
    }
    .first_section{
        display: flex;
        align-items: flex-start;
        justify-content: space-between;
        background: #FBFEE9;
         padding: 40px;
    }
   .first_section .left_div{
       text-align: left;
       width: 50%;
    }
    .first_section .left_div h2{
        font-weight: 700;
    }
    .first_section .left_div h4{
        margin-bottom:50px;
    }
    .first_section .left_div ul{
        padding-left:15px;
    }
    .first_section .right_div{
        display: flex;
        flex-direction: column;
       text-align: left;
       width: 50%;
    }
    .first_section .right_div h2{
        margin-bottom: 50px;
    }
    .first_section .right_div .boxes{
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
        width: 100%;
        overflow-x: hidden;
    }
    .first_section .right_div .boxes .box {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content:center;
        width:33%;
    }
    .first_section .right_div .boxes .box p{
        color: #284948;
    }
    .first_section .right_div .boxes .box .box_inner{
        padding: 20px;
        margin-bottom: 10px;
        border-radius: 5px;
    }
    .first_section .right_div .boxes .box:nth-child(1) .box_inner,
    .first_section .right_div .boxes .box:nth-child(4) .box_inner{
        background: #41345F;
    }
    .first_section .right_div .boxes .box:nth-child(2) .box_inner,
    .first_section .right_div .boxes .box:nth-child(5) .box_inner{
        background: linear-gradient(180deg, #44965B 0%, #3E8C58 100%);
    }
    .first_section .right_div .boxes .box:nth-child(3) .box_inner,
    .first_section .right_div .boxes .box:nth-child(6) .box_inner{
        background: #DD7A1D;
    }
    .first_section .right_div .boxes .box:nth-child(4),
    .first_section .right_div .boxes .box:nth-child(5),
    .first_section .right_div .boxes .box:nth-child(6){
        position: relative;
        left:50px;
    }
    .first_section .right_div .boxes .box .box_inner img{
        width: 100%;
        height: 50px;
        object-fit: cover;
    }
    @media screen and (min-width:300px) and (max-width:500px) {
        .first_section{
            flex-direction: column;
        } 
        .first_section .left_div,.first_section .right_div{
            width:100%;
        }
        .first_section .left_div{
            text-align: center;
            margin-bottom: 30px;
        }
        .first_section .left_div h4{
            margin-bottom: 20px;
        }
        .first_section .right_div h2{
            margin-bottom: 20px;
        }
        .first_section .right_div .boxes .box:nth-child(4),
        .first_section .right_div .boxes .box:nth-child(5),
        .first_section .right_div .boxes .box:nth-child(6){
            left: 0px;   
        }
    }
        @media screen and (min-width:501px) and (max-width:768px) {
            .first_section{
                flex-direction: column;
            } 
            .first_section .left_div,.first_section .right_div{
                width:100%;
            }
            .first_section .left_div{
                text-align: center;
                margin-bottom: 30px;
            }
            .first_section .left_div h4{
                margin-bottom: 20px;
            }
            .first_section .right_div{
                text-align:center;
            }
            .first_section .right_div h2{
                margin-bottom: 20px;
            }
            .first_section .right_div .boxes .box:nth-child(4),
            .first_section .right_div .boxes .box:nth-child(5),
            .first_section .right_div .boxes .box:nth-child(6){
                left: 0px;   
            }
        }
</style>
