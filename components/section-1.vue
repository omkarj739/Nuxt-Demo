<template>
    <section class="first_section">
          <div class="title">
            <h2>LOOK AFTER THE PEOPLE, WHO LOOK AFTER YOUR BUSINESS.</h2>
            <h2 class="health">HEALTH WELLNESS.</h2>
            <v-btn color="secondary" style="margin-top:20px;">Request Demo</v-btn>
          </div>
          <div class="right_side">
            <img src="../images/section_1.png" alt="img">
          </div>
    </section>
</template>

<script>
export default {
  name: 'section_1'
}
</script>
<style scoped>
 .first_section {
    width:100%;
    height:500px;
    display: flex;
    align-items:center;
    overflow:hidden;
  }
  .first_section .title{
    width:50%;
    align-items:center;
    color: black;
    z-index: 2;
    padding: 0 20px 0 50px;
  }
  .first_section .title h2{
    color:#284948;
    font-weight: 400; 
    margin-top: 50px;
  }
  .first_section .title .health{
     margin-top: 90px;
     font-weight: 600;
  }
  .first_section div{
    width:50%;
    height: 100%;
  }
  .first_section .right_side img{
    width: 100%;
    height: 100%;
    object-fit:contain;
    position: relative;
    right: 60%;
    transform:scale(2);
    z-index: 1;
  }
  @media screen and (min-width:300px) and (max-width:500px){
    .first_section{
      flex-direction:column;
    }
    .first_section .title .health{
      margin-top:10px;
    }
    .first_section .right_side{
      width:100%;
    }
    .first_section .title{
      width:100%;
      text-align:center;
      padding: 20px;
    }
    .first_section .right_side img{
      right: 25%;
      transform:scale(1.2);
    }
  }
  @media screen and (min-width:501px) and (max-width: 768px){
    .first_section{
      flex-direction:column;
    }
    .first_section .title .health{
      margin-top:10px;
    }
    .first_section .right_side{
      width:100%;
    }
    .first_section .title{
      width:100%;
      text-align:center;
      padding: 20px;
    }
    .first_section .right_side img{
      right: 20%;
      margin-top: -7px;
      transform:scale(1);
    }
  }
  @media screen and (min-width:769px) and (max-width: 1024px){
    .first_section{
      height:340px;
    }
    .first_section .title .health{
      margin-top:10px;
    }    
    .first_section .right_side img{
      margin-top: -7px;
    }
  }
  @media screen and (min-width:1024px) and (max-width: 1200px){
    .first_section{
      height:420px;
    }
  }
   @media screen and (min-width:1201px) and (max-width: 1500px){
    .first_section{
      height: 500px;
    }  
  }
</style>
