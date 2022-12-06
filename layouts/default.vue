<template>
  <v-app class="light">
    <v-navigation-drawer 
      v-model="drawer"
      :mini-variant="miniVariant"
      :clipped="clipped"
      fixed
      app
    >
      <v-list>
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          router
          exact
        >
          <v-list-item-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <header class="desktop_view">
      <v-container>
        <ul>
          <li v-for="item in items"><a nuxt to="/">{{item.title}}</a></li>
          <li>
            <v-btn color="link" nuxt to="/">
              Sign Up
            </v-btn>
          </li>
          
        </ul>
      </v-container>
    </header>  
    <v-app-bar class="mobile_view"
      :clipped-left="clipped"
      fixed
      app
    >
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" />
      <v-btn
        icon
        @click.stop="miniVariant = !miniVariant"
      >
      </v-btn>
    </v-app-bar>
    <v-main>
      <section>
        <Nuxt />
      </section>
    </v-main>
    <v-navigation-drawer
      v-model="rightDrawer"
      :right="right"
      temporary
      fixed
    >
      <v-list>
        <v-list-item @click.native="right = !right">
          <v-list-item-action>
            <v-icon light>
              mdi-repeat
            </v-icon>
          </v-list-item-action>
          <v-list-item-title>Switch drawer (click me)</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-footer :absolute="!fixed" app class="footer">
    <div class="footer_main">
      <div class="first_col">
        <h2 class="c_name">Reach Out to Us</h2>
        <p class="c_para">Lorem epsum Pvt Ltd.</p>
        <div class="info">
          <div class="address">
             <v-icon class="icon">mdi-map-marker</v-icon>
             <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Lorem ipsum dolor sit amet, consectetur adipiscing elit. </p>
          </div>
          <div class="address">
            <v-icon class="icon">mdi-phone</v-icon>
            <p>+91452547452</p>
          </div>
          <div class="address">
            <v-icon class="icon">mdi-email</v-icon>
            <p>loremepsum@gmail.com</p>
          </div>
        </div>
      </div>
      <div class="sec_col">
        <h4 class="c_name">About</h4>
        <ul class="info">
            <li>Contact Us</li>
            <li>Contact Us</li>
            <li>Contact Us</li>
            <li>Contact Us</li>
            <li>Contact Us</li>
        </ul>
      </div>
      <div class="third_col">
        <h4 class="c_name">Policy Info</h4>
        <ul class="info">
            <li>Contact Us</li>
            <li>Contact Us</li>
            <li>Contact Us</li>
        </ul>
      </div>
      <div class="fourth_col">
        <h4 class="c_name">Policy Info</h4>
        <ul class="info">
            <li>Contact Us</li>
            <li>Contact Us</li>
            <li>Contact Us</li>
        </ul>
        <button class="">Request Demo</button>
      </div>
      <div class="fifth_col">
        <h4 class="c_name">Subscribe Our Newsletter</h4>
        <div class="input_div">
          <input type="text" placeholder="Enter Your Email" />         
          <v-icon class="input_btn">mdi-arrow-right</v-icon>
        </div>
        <p>Register now to get updates on promotions and coupons or Download App</p>
      </div>
    </div>
    <div class="copyrights">
      <span>&copy; Copyright {{ new Date().getFullYear() }} UniteCloud</span>
    </div>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',
  data () {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: 'mdi-apps',
          title: 'home',
          to: '/'
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'For Engineers',
          to: '/'
        },
         {
          icon: 'mdi-chart-bubble',
          title: 'Multi-Vitamins',
          to: '/'
        },
         {
          icon: 'mdi-apps',
          title: 'Books',
          to: '/'
        }
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Vuetify.js'
    }
  }
}
</script>
<style scoped>
  .light{
    background-color:#FFFFFF !important;
  }
  .mobile_view{
    display:none;
  }
  .desktop_view{
    display: block;
    background: white;
    box-shadow: 0px 2px 4px -1px rgb(0 0 0 / 20%), 0px 4px 5px 0px rgb(0 0 0 / 14%), 0px 1px 10px 0px rgb(0 0 0 / 12%);
  }
  .desktop_view ul{
    display: flex;
    justify-content: flex-end;
    align-items: center;
    list-style: none;
    padding: 5px 0;
  }
   .desktop_view ul li a{
    color: black;
  }
  .desktop_view ul li{
    color: black;
    padding:0 0 0 20px;
  }
  .v-navigation-drawer__content{
    display:none !important;
  }
  .footer{
    display: flex;
    flex-direction: column;
    background-color: #284948;
    width: 100%;
    color: white;
    padding: 40px;
  }
  .footer .footer_main{
    width: 100%;
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    margin-bottom: 30px;
  }
  .footer div{
    padding:0px 10px;
  }
  .footer .first_col{
    display: flex;
    flex-direction:column;
    text-align: left;
    width: 30%;
  }
  .footer .first_col h2.c_name{
    font-weight: 600;
  }
  .footer .first_col .c_para{
    margin-bottom: 30px;
  }
  .footer .first_col .info{
    background-color: transparent !important;
  }
  .footer .first_col .info .address{
    display: flex;
    align-items: center;
    margin-bottom:10px; 
  }
  .footer .first_col .info .address p{
    margin-bottom:0px; 
  }
  .footer .first_col .info .icon{
    color: white;
    margin-right: 10px;
    color: #F28737;
  }
  .footer .sec_col,
  .footer .third_col,
  .footer .fourth_col{
    width: 15%;
  }
  .footer .fifth_col{
    width: 25%;
  }
  .footer .sec_col h4,
  .footer .third_col h4,
  .footer .fourth_col h4{
    font-weight: 700;
    margin-bottom:20px;
  }
  .footer .sec_col ul,
  .footer .third_col ul,
  .footer .fourth_col ul{
    list-style: none;
    background-color: transparent !important;
    padding-left:0px;
  }
  .footer .fourth_col ul{
    margin-bottom: 25px;
  }
  .footer .fourth_col button{
    padding: 6px 20px;
    background: #F28737;
    height: 32px;
    font-size: 14px;
    border-radius: 5px;
    color: white;
  }
  .footer .fifth_col input{
    margin: 20px 0;
    background-color: white;
    padding:10px;
    border-radius: 5px 0 0 5px;
    border:none;
    outline: none;
  }
  .footer .fifth_col .input_btn{
    background: #F28737;
    padding: 10px 6px;
    position: relative;
    left: -4px;
    top: -1px;
    border-radius: 0 5px 5px 0;
  }
  .footer .copyrights{
    width: 100%;
    text-align: right;
  }
  @media screen and (min-width:300px) and (max-width:768px){
    .mobile_view{
      display:block;
    }
     .desktop_view{
      display: none;
    }
     .v-navigation-drawer__content{
      display:block;
    }
  }
  @media screen and (min-width:769px) and (max-width:2000px) {
    .v-navigation-drawer__content{
      display:none !important;
    }
  }
  @media screen and (min-width:300px)  and (max-width:500px){
    .footer{
      padding: 10px;
    }
     
    .footer .first_col,
    .footer .sec_col,
    .footer .third_col,
    .footer .fourth_col,
    .footer .fifth_col{
      width: 100%;
      margin-bottom: 20px;
    }
    .footer .fifth_col h4,
    .footer .sec_col h4,
    .footer .third_col h4,
    .footer .fourth_col h4{
    margin-bottom: 10px;
    font-size: 18px;
  }
    .footer .sec_col,
    .footer .third_col,
    .footer .fourth_col{
      width: 50%;
    }
    .footer .copyrights{
      text-align: center;
    }
  }
  @media screen and (min-width:501px)  and (max-width:768px){
    .footer{
      padding: 30px 10px;
    }
    .footer .first_col{
      width: 100%;
      margin-bottom: 20px;
    }
    .footer .footer_main{
       align-items: baseline;
     }
    .footer .fifth_col h4,
    .footer .sec_col h4,
    .footer .third_col h4,
    .footer .fourth_col h4{
    margin-bottom: 10px;
    font-size: 18px;
  }
    .footer .sec_col,
    .footer .third_col,
    .footer .fourth_col{
      width: 50%;
      margin-bottom: 20px;
    }
    .footer .fifth_col{
      width: 100%;
      margin-bottom: 20px;
    }
    .footer .copyrights{
      text-align: center;
    }
  }
  @media screen and (min-width:769px)  and (max-width:1024px){
    .footer{
      padding: 30px 10px;
    }
    .footer .first_col{
      width: 50%;
      margin-bottom: 20px;
    }
     .footer .footer_main{
       align-items: baseline;
     }
    .footer .fifth_col h4,
    .footer .sec_col h4,
    .footer .third_col h4,
    .footer .fourth_col h4{
      margin-bottom: 10px;
      font-size: 18px;
  }
    .footer .sec_col,
    .footer .third_col{
      width: 20%;
      margin-bottom: 20px;
    }
    .footer .fourth_col{
       width: 30%;
      margin-bottom: 20px;
    }
    .footer .fifth_col{
      width: 50%;
      margin-bottom: 20px;
    }
    .footer .copyrights{
      text-align: center;
    }
  }
  @media screen and (min-width:1024px)  and (max-width:2000px){
    .v-navigation-drawer--fixed{
      display:none !important;
    }
    .v-main{
      padding-left:0px !important;
    }
  }
</style>
