<template>
    <section class="first_section">
        <h2 style="">TRUSTED BY MANY</h2>
        <div class="color_boxes">
            <div class="box box_1"></div>
            <div class="box box_2"></div>
            <div class="box box_3"></div>
            <div class="box box_4"></div>
        </div>
    </section>
</template>

<script>
export default {
  name: 'section_2'
}
</script>
<style scoped>
  .first_section{
    background:#FBFEE9;
    padding: 40px 0;
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
      align-items:center;
      margin-top:20px;
    }
    .first_section .color_boxes .box{
      width: 18%;
      height: 100px;
      padding: 2rem;
      margin: 10px 30px;
    }
  .first_section .color_boxes .box_1{
    background:#284948;
  }
  .first_section .color_boxes .box_2{
     background:#DD7A1D;
  }
  .first_section .color_boxes .box_3{
     background: #3E8C58;
  }
  .first_section .color_boxes .box_4{
     background: #41345F;
  }
</style>
