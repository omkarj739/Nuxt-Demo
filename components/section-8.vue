<template>
  <section class="first_section">
        <h1 class="title">WHAT WE OFFER</h1>
        <div class="offer_list">
            <div class="boxes">
                <div v-for="item in items" class="box">
                    <div class="box_inner">
                        <img src="../images/dimension_icon_1.png" alt="img">
                    </div>
                    <p>{{item.title}}</p>
                </div>
            </div>
        </div>
  </section>
</template>

<script>
export default {
    name:'section-8',
    data(){
        return{
            items:[
                {title : 'Ayurveda'},
                {title : 'Ayurveda'},
                {title : 'Ayurveda'},
                {title : 'Ayurveda'},
                {title : 'Ayurveda'},
                {title : 'Ayurveda'},
                {title : 'Ayurveda'},
                {title : 'Ayurveda'}
            ]
        }
    }
}
</script>

<style scoped>
    .first_section{
        padding: 40px;
        background-image: url('../images/bg_img_2.png');
        background-position: center;
        background-repeat: no-repeat;
        background-size: cover;
        text-align: center;
    }
    .first_section h1.title{
        margin-bottom: 40px;
        color:#284948;
        font-weight: 700;
    }
    .first_section .boxes{
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
        width: 100%;
        overflow-x: hidden;
    }
    .first_section .boxes .box {
        display: flex;
        align-items: center;
        justify-content:center;
        width:25%;
        margin-bottom:20px;
    }
    .first_section .boxes .box p{
        color: #284948;
        margin-left: 10px;
    }
    .first_section .boxes .box .box_inner{
        padding: 15px;
        margin-bottom: 10px;
        border-radius: 5px;
        background: #D2E289;
    }
     .first_section .boxes .box .box_inner img{
         object-fit: cover;
         width: 70px;
         height: 70px;
     }
     @media screen and (min-width:300px) and (max-width:500px) {
         .first_section .boxes .box{
             width: 48%;
             flex-direction: column;
         }
     }
     @media screen and (min-width:501px) and (max-width:768px) {
         .first_section .boxes .box{
             width: 48%;
             flex-direction: column;
         }
    }
</style>