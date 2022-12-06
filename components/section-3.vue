<template>
    <section class="first_section">
        <h2 style="">LIFECYCLE COST OF A DISEASE</h2>
        <div class="color_boxes">
            <div v-for="items in items" class="box">
                <div class="box_1"><p>demo</p></div>
                <p>{{items.lifeStyles}}</p>
            </div>
            <v-icon light>mdi-plus</v-icon>
            <div class="last_box">
                <div class="box_4"><p>demo</p></div>
                <p>Decrease quality of life, pain, anxiety, incovenience </p>
            </div>
        </div>
    </section>
</template>

<script>
export default {
  name: 'section_3',
  data(){
      return{
          items:[
              {
                  lifeStyles:'Healthcare & Medical Cost'
              },
              {
                  lifeStyles:'Decrease quality of life, pain, anxiety, incovenience &'
              },
              {
                  lifeStyles:'Decrease quality of life, pain, anxiety, incovenience &'
              }
          ]
      }
  }
}
</script>
<style scoped>
    .first_section{
        background:url('../images/bg_img.png');
        background-repeat:no-repeat;
        background-position:center;
        background-size:cover;
         padding: 50px 20px 130px;
        display:flex;
        flex-direction: column;
        justify-content:center;
        align-items:center;
    }
    .first_section h2{
        font-weight:800;
        color:#284948;
    }
    .first_section .color_boxes{
    width: 100%;
    display:flex;
    flex-wrap:wrap;
    justify-content:center;
    align-items:baseline;
    margin-top:20px;
  }
  .first_section .color_boxes .box .box_overlay{
      position: absolute;
      height:100%;
      width:100%;
      background:#00000060;
  }
  .first_section .color_boxes .box{
    width: 18%;
    height: 100px;
    margin: 0px 30px;
  }
  .first_section .color_boxes .box .box_1 p{
       color:white;
   }
   .first_section .color_boxes .box p{
       margin-top: 20px;
       color:#284948;
   }
    .first_section .color_boxes .box_1{
         display:flex;
        justify-content:center;
        align-items:center;
        padding: 2rem;
        background:url('../images/box_img.png');
        background-repeat:no-repeat !important;
        background-position:center !important;
        background-size:cover !important;
        border-radius: 20px;
    }
    .first_section .color_boxes .last_box{
         width: 23%;
        height: 100px;
        margin: 0px 30px;
    }
    .first_section .color_boxes .last_box .box_4 p{
       color:white;
    }
    .first_section .color_boxes .last_box p{
       margin-top: 20px;
       color:#284948;
    }
    .first_section .color_boxes .box_4{
         display:flex;
        justify-content:center;
        align-items:center;
        padding: 2rem;
        background:url('../images/box_img.png');
        background-repeat:no-repeat !important;
        background-position:center !important;
        background-size:cover !important;
        border-radius: 20px;
    }
  .first_section .color_boxes .box_2{
    background:url('../images/box_img.png');
  }
  .first_section .color_boxes .box_3{
     background:url('../images/box_img.png');
  }
  .first_section .color_boxes .box_4{
     background:url('../images/box_img.png');
  }
  @media screen and (min-width:300px) and (max-width:500px){
       .first_section {
        padding: 20px 30px;
          text-align:center;
      }
      .first_section .color_boxes .box{
          width:100%;
          height: 190px;
          margin-bottom: 10px;
      }
      .first_section .color_boxes .last_box{
          width:100%;
          height: 190px;
          margin-bottom: 10px;
      }
  }
  @media screen and (min-width:501px) and (max-width:768px){
       .first_section {
        padding: 20px 30px;
          text-align:center;
      }
      .first_section .color_boxes .box{
          width:35%;
          height: 230px;
          margin-bottom: 10px;
      }
      .first_section .color_boxes .last_box{
           width:35%;
          height: 230px;
          margin-bottom: 10px;
      }
  }
  @media screen and (min-width: 769px) and (max-width: 1024px){
       .first_section {
        padding: 20px 30px;
          text-align:center;
      }
      .first_section .color_boxes .box{
          width:35%;
          height: 230px;
          margin-bottom: 10px;
      }
      .first_section .color_boxes .last_box{
           width:35%;
          height: 230px;
          margin-bottom: 10px;
      }
  }
  @media screen and (min-width: 1025px) and (max-width: 1200px){
       .first_section {
            padding: 20px 30px;
          text-align:center;
      }
      .first_section .color_boxes .box{
          width: 20%;
          height: 230px;
          margin-bottom: 10px;
      }
      .first_section .color_boxes .last_box{
           width:27%;
          height: 230px;
          margin-bottom: 10px;
      }
  }
   @media screen and (min-width: 1201px) and (max-width: 1500px){
       .first_section {
            padding: 50px 30px;
          text-align:center;
      }
      .first_section .color_boxes .box{
          width: 17%;
          height: 230px;
          margin-bottom: 10px;
      }
      .first_section .color_boxes .last_box{
           width:25%;
          height: 230px;
          margin-bottom: 10px;
      }
  }
</style>
