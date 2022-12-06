<template>
  <section class="first_section">
      <div class="lap_div">
          <img src="../images/lap_img.png" alt="">
      </div>
      <div class="info">
          <h1>COMPLETE DASHBOARD FOR YOUR COMPANY</h1>
          <button>Request Demo</button>
      </div>
  </section>
</template>

<script>
export default {
    name: 'section-9'
}
</script>

<style scoped>
    .first_section{
        background: linear-gradient(90.05deg, #284948 1.22%, #141414 98.84%);
        display: flex;
        justify-content: center;
        align-items: center;
        text-align: center;
        margin-bottom: 90px;
    }
    .first_section .lap_div{
        width: 50%;
    }
    .first_section .lap_div img{
        width: auto;
        height: 300px;
        object-fit: cover;
        position: relative;
        top: 80px;
        margin-bottom: 20px;
    }
    .first_section .info{
        width: 50%;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: flex-start;
        text-align: left;
        background-color: transparent !important;
    }
     .first_section .info h1{
         font-size: 40px;
     }
    .first_section .info button{
        background: #F28737;
        color: white;
        padding: 7px 20px;
        height: 40px;
        border-radius:5px;
        margin-top: 10px;
    }
    @media screen and (min-width:300px) and (max-width:500px) {
         .first_section{
             flex-direction: column;
             margin-bottom: 0px;
             padding: 35px 15px;
         }
        .first_section .lap_div,
            .first_section .info{
            width: 100%;
            text-align: center;
            align-items: center;
        }
        .first_section .lap_div img{
            top:0px;
            height: 200px;
        }
    }
    @media screen and (min-width:501px) and (max-width:768px) {
         .first_section{
             flex-direction: column;
             margin-bottom: 0px;
             padding: 35px 15px;
         }
        .first_section .lap_div,
            .first_section .info{
            width: 100%;
            text-align: center;
            align-items: center;
        }
        .first_section .lap_div img{
            top:0px;
        }
    }
    @media screen and (min-width:768px) and (max-width:1024px) {
        .first_section{
             padding: 35px 15px;
             margin-bottom: 40px;
         }
         .first_section .lap_div img{
             height: 200px;
         }    
    }
</style>