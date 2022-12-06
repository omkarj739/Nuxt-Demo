<template>
    <section class="first_section">
        <h2 class="title">HOW DOES THIS WORK ?</h2>
        <div class="steps">
            <div class="step_1 step_1_1">
                <div class="step_info">
                    <h2>Step 1</h2>
                    <p class="para_first">Lorem ipsum dolor sit amet, consectetur adipiscing elit. </p>
                    <div class="line"></div>
                    <p class="para_sec">Lorem ipsum dolor sit amet, consectetur adipiscing elit. </p>
                </div>
                <v-icon class="arrow">mdi-chevron-left</v-icon>
            </div>
            <div class="step_1 step_1_2">
                <div class="step_info">
                    <h2>Step 1</h2>
                    <p class="para_first">Lorem ipsum dolor sit amet, consectetur adipiscing elit. </p>
                    <div class="line"></div>
                    <p class="para_sec">Lorem ipsum dolor sit amet, consectetur adipiscing elit. </p>
                </div>
                <v-icon class="arrow">mdi-chevron-up</v-icon>
            </div>
            <div class="step_1 step_1_3">
                <v-icon class="arrow">mdi-chevron-right</v-icon>
                <div class="step_info">
                    <h2>Step 1</h2>
                    <p class="para_first">Lorem ipsum dolor sit amet, consectetur adipiscing elit. </p>
                    <div class="line"></div>
                    <p class="para_sec">Lorem ipsum dolor sit amet, consectetur adipiscing elit. </p>
                    <button class="req_btn">Request Demo</button>
                </div>
            </div>
        </div>
        <div class="meditation">
            <img src="../images/meditation_img.png" alt="img">
        </div>
    </section>
</template>

<script>
export default {
    name : 'section_7',
}
</script>

<style scoped>
    .first_section{
        color:#284948;
        padding: 40px;
        display: flex;
        flex-direction: column;
        text-align: center;
        background-color: #F9F9F9;
    }
    .first_section h2.title{
        margin-bottom: 20px;
        font-weight: 700;
    }
    .first_section .steps{
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
    }
    .first_section .steps .step_1{
        display: flex;
        align-items: flex-end;
        justify-content: center;
        width: 33%;
    }
      .first_section .steps .step_1:hover .step_info{
        box-shadow: rgba(0, 0, 0, 0.25) 0px 25px 50px -12px;
    }
    .first_section .steps .step_1:hover .arrow{
        font-size: 30px;
    }
    .first_section .steps .step_1 .step_info{
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        padding:10px;
        transition: all 0.3s;
    }
    .first_section .steps .step_1 .step_info h2{
        color:#DD7A1D;
        font-weight: 700;
     }
     .first_section .steps .step_1 .step_info .para_first{
         color: #000;
     }
     .first_section .steps .step_1 .step_info .line{
         padding: 1px;
         width:100%;
         background-color:#DD7A1D;
         margin-bottom: 9px;
     }
     .first_section .steps .step_1_1,
     .first_section .steps .step_1_3{
         position: relative;
         top: 100px;
     }
     .first_section .steps .step_1_2{
         flex-direction: column;
         align-items: center;
     }
     .first_section .steps .step_1_3 .req_btn{
         background-color:#DD7A1D;
         color: white;
         padding: 7px 20px;
         border-radius:5px;
         width:200px;
     }
     .first_section .steps .step_1 .arrow{
         color:#DD7A1D;
         padding: 0 10px;
         transition: all 0.3s;
     }
    .first_section .steps .step_1 .step_info .para_sec{
         color: gray;
     }
     .first_section .meditation {
         text-align: center;
     }
     .first_section .meditation img{
         object-fit: cover;
         width: 300px;
         height: 300px;
    }
    @media screen and (min-width:300px) and (max-width:500px) {
         .first_section .steps .step_1{
             width:100%;
             margin-bottom: 20px;
         }  
        .first_section .steps .step_1_1,
        .first_section .steps .step_1_3{
            position: unset;
        }
        .first_section .steps .step_1 .arrow{
            display: none;
        } 
    }
     @media screen and (min-width:501px) and (max-width:768px) {
         .first_section .steps .step_1{
             width:100%;
             margin-bottom: 20px;
         }  
        .first_section .steps .step_1_1,
        .first_section .steps .step_1_3{
            position: unset;
        }
        .first_section .steps .step_1 .arrow{
            display: none;
        } 
    }
</style>