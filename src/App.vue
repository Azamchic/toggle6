<template>
  <header class="header">
    <div class="navbar">
      <div class="logo rounded-md"><a href="#">CAR MUSIC</a></div>
      <ul class="links">
        <li><a href="hero">HOME</a></li>
        <li><a href="about">ABOUT</a></li>
        <li><a href="services">SERVICES</a></li>
        <li><a href="contact">CONTACT</a></li>
      </ul>
      <a href="#" class="action_btn">Get Started</a>
      <div class="toggle_btn w-[20px] h-[10px]" :onclick="toggleMenu">
        <i class="fa-solid fa-bars text-3xl"></i>
      </div>
    </div>
    <div class="dropdown_menu" v-if="isActive">
      <li><a href="hero">HOME</a></li>
        <li><a href="about">ABOUT</a></li>
        <li><a href="services">SERVICES</a></li>
        <li><a href="contact">CONTACT</a></li>
        <li><a href="#" class="action_btn">Get Started</a></li>
    </div>
    
    <div class="text_logo">
      <h1 class="text">CAR MUSIC</h1>
      <p class="layout" >Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vitae orci urna amet penatibus.</p>
      <button class="btn">Наши услуги</button>
    </div>

  </header>

  
</template>

<script>
export default {
  data(){
    return{
      isActive: false
    }
  },

  methods: {
    toggleMenu() {
    this.isActive = !this.isActive
}
    }
  }



</script>

<style>

  li{
    list-style: none;
  }

  a{
    text-decoration: none;
    color: #000;
    font-size: 30px;
  }
  a:hover{
    color: red;
    transition: 1s;
  }

  header{
    position: relative;
    padding: 0 2rem;
  }
  .navbar{
    width: 100%;
    height: 60px;
    margin: 0 auto;
    display: flex;
    align-items: center;
    justify-content: space-between;
  }

  .navbar .logo a{
    font-size: 40px;
    font-weight: bold;
    color: red;
  }

  .navbar .links{
    display: flex;
    gap: 2rem;
    color: #fff;
    font-weight: 500;
  }

  .navbar .toggle_btn{
    color: red;
    font-size: 1.5rem;
    cursor: pointer;
    display: none;
  }

  .action_btn{
    background-color: red;
    color: green;
    padding: 0.5rem 1rem;
    border: none;
    outline: none;
    border-radius: 20px;
    font-size: 0.8rem;
    font-weight: bold;
    cursor: pointer;
    width: 140px; 
    height: 50px;
    font-size: 20px;
  }

  .action_btn:hover{
    scale: 1.05;
    color: #fff ;
  }

  .action_btn{
    scale: 0.95;
  }

  /* dropdown */
  .dropdown_menu{
    display: none;
    position: absolute;
    right: 2rem;
    top: 60px;
    height: 0;
    width: 300px;
    background: rgba(255, 255, 255, 0.1);
    backdrop-filter: blur(15px);
    border-radius: 10px;
    overflow: hidden;
    transition: 0.5s;
    color: red;
    
  }

  .dropdown_menu{
    height: 280px;

  }

  .dropdown_menu li{
    padding: 0.7rem;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .dropdown_menu .action_btn{
    width: 100%;
    display: flex;
    justify-content: center;
  }

  .header{
    width: 100%;
    height: 800px;
    background: url(./assets/image/car_music.png) no-repeat center / cover;
    margin: 0 auto;
  }

    .header .text_logo{
      width: 500px;
      margin: 0 auto;
    }

    .header .text_logo .layout{
      color: #fff;
      width: 400px;
      height: 97px;
      font-weight: 500;
      text-align: center;
      font-size: 24px;
      margin: 0 0 0 30px;
    }

    .header .text_logo .text{
      font-size: 90px;
      color: red;
      font-weight: 500;
      margin-top: 200px;
      margin-left: 20px;
    }

    

    .header .text_logo .btn{
      color: #fff;
      background: red;
      width: 110px;
      height: 61px;
      border: 2px solid red;
      cursor: pointer;
      margin: 30px 0 0 169px;
    }


    /* media */

    @media screen and (max-width: 967px){

      .header{
        max-width: 967px;
      }

      .header .navbar .links{
        display: none;
      }

      .header .navbar .action_btn{
        display: none;
      }

      .header .dropdown_menu{
        display: block;
      }

      .header .navbar .toggle_btn{
        display: block;
      }
    };


    @media screen and (max-width: 768px) {
      .header{
        max-width: 768px;
      }

      .header .navbar .links{
        display: none;
      }

      .header .navbar .toggle_btn{
        display: block;
      }

      .dropdown_menu{
        display: block;
      }
      .header .navbar .action_btn{
        display: none;
      }
    };


    @media screen and (max-width: 541px){

      .header{
        max-width: 541;
      }

      .header .text_logo{
        max-width: 540px;
      }

      .header .text_logo .text{
        margin-left: 5px;
      }

    };


    @media screen and (max-width: 530px){
      .header{
        max-width: 530px;
      }
    };
    
    @media screen and (max-width: 521px){
      .header{
        max-width: 521px;
      }

      .header .text_logo{
        max-width: 520px;
        margin-left: -20px;
      }
    };


    @media screen and (max-width: 510px){
      .header{
        max-width: 510px;
      }

      .header .text_logo{
        max-width: 510px;
        margin-left: -30px;
      }
    };

    @media screen and (max-width: 500px){
      .header{
        max-width: 500px;
      }

      .header .text_logo{
        max-width: 400px;
        margin-left: -40px;
      }

      .header .text_logo .text{
        font-size: 40px;
        margin-left: 110px;
      }

      .header .navbar .toggle_btn{
        margin-right: 30px;
      }
    };
    

    @media screen and (max-width: 430px) {
      .header{
        max-width: 430px;
      }
    };


   
    @media screen and (max-width: 425px){
      .header{
        display: block;
        max-width: 425px;
      }

      .header .text_logo{
        max-width: 400px;
      }
      
      .header .text_logo .text{
        max-width: 400x;
        font-size: 50px;
        margin-left: 80px;
      }

      .header .text_logo .layout{
        max-width: 400px;
        font-size: 20px;
        margin-left: 20px;
      }

      .header .text_logo .btn{
        margin-left: 170px;
      }
    };

    @media screen and (max-width: 410px){
      .header .navbar .logo{
        display: none;
      }

      .header .text_logo{
        max-width: 410px;
        margin-right: 20px;
      }

      .header .text_logo .layout{
        max-width: 400px;
        margin-left: 10px;
      }

    };

    @media screen and (max-width: 400px){
      .header{
        max-width: 400px;
      }

      .header .text_logo{
        max-width: 300px;
      }

      .header .text_logo .text{
        width: 300px;
        font-size: 40px;
      }

      .header .text_logo .layout{
        width: 300px;
        font-size: 24px;
        font-weight: 400;
        margin-left: 40px;
      }

      .header .text_logo .btn{
        margin-top: 100px;
        margin-left: 150px;
      }
    };

    @media screen and (max-width: 370px){
      .header{
        max-width: 370px;
      }

      .header .text_logo{
        max-width: 250px;
      }

      .header .text_logo .text{
        max-width: 250px;
      }
    };

    @media screen and (max-width: 340px){
      .header{
        max-width: 340px;
      } 

      .header .text_logo{
        max-width: 340px;
      }

      .header .text_logo .text{
        margin-left: 50px;
      }

      .header .text_logo .layout{
        margin-left: 20px;
      }

      .header .text_logo .btn{
        margin-left: 120px;
      }
    }

    @media screen and (max-width: 330px){
      .header {
        max-width: 340px;
      }

      .header .text_logo{
        max-width: 330px;
        margin-left: -20px;
      }

      .header .text_logo .text{
        max-width: 310px;
        margin-left: 30px;
      }

      .header .text_logo .layout{
        max-width: 310px;
        font-size: 20px;
        margin-left: -5px;
      }

      .header .text_logo .btn{
        margin-top: 20px;
        margin-left: 80px;
      }
    }

   
    
  


</style>