<template>
    <section class="first_section">
        <div class="left">
            <div class="line"></div>
            <h3 class="title_1">WE HEAL YOU </h3>
            <h2 class="title_2">NATURALLY</h2>
            <div class="line"></div>
        </div>
        <div class="right">
            <div class="boxes">
                <div class="box" v-for="item in items">
                    <div class="box_inner">
                        <img src="../images/bottle_img.png" alt="img">
                    </div>
                    <p>{{item.titles}}</p>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
  name: 'section_4',
  data(){
      return{
          items:[
              {titles:'Ayurveda'},
              {titles:'Homeopathy'},
              {titles:'Yoga'},
              {titles:'Naturopathy'},
              {titles:'Meditation'},
              {titles:'Physiotherapy'},
              {titles:'Nutrition'},
              {titles:'Psychology'}
          ]
      }
  }
}
</script>
<style scoped>
    .first_section{
        background:url('../images/bg_img_2.png');
        background-repeat:no-repeat;
        background-position:center;
        background-size:cover;
        padding: 80px 50px;
        display:flex;
        justify-content:center;
        align-items:center;
    }
    .first_section .left{
        width:30%;
        display:flex;
        flex-direction:column;
        justify-content:center;
    }
    .first_section .left .line{
        padding:2px;
        background:#F28737;
    }
    .first_section .left .title_1{
        font-weigth:700;
        margin: 20px 0;
        color: #284948;
    }
    .first_section .left .title_2{
        font-weigth:500;
        color: #284948;
        margin-bottom: 20px;
    }
    .first_section .right{
        width:70%;
    }
    .first_section .right .boxes{
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
    }
    .first_section .right .boxes .box {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content:center;
        width: 22%;
    }
    .first_section .right .boxes .box p{
        color: #284948;
    }
    .first_section .right .boxes .box .box_inner{
        background: linear-gradient(180deg, #284948 0%, #3E8C58 100%);
        padding: 20px 35px;
        margin-bottom: 10px;
        border-radius: 5px;
    }
    .first_section .right .boxes .box .box_inner img{
        width: 100%;
        height: 50px;
        object-fit: cover;
    }
    @media screen and (min-width:300px) and (max-width:500px){
        .first_section{
            flex-direction:column;
        }
        .first_section .left,
        .first_section .right{
             width: 100%;
         }
         .first_section .right .boxes{
             margin-top: 20px;
         }
          .first_section .right .boxes .box {
              width: 50%;
          }
    }
    @media screen and (min-width:501px) and (max-width:768px){
        .first_section{
            flex-direction:column;
        }
        .first_section .left,
        .first_section .right{
             width: 100%;
         }
         .first_section .right .boxes{
             margin-top: 20px;
         }
          .first_section .right .boxes .box {
              width: 25%;
          }
    }
</style>
