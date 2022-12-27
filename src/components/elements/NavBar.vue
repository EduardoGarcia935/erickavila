<template>
  <nav :class="{sticky : scrolled}" ref="navbar" id="nav">

    <div class="group1">
      <div class="img-container">
        <img src="../../assets/images/logo.png" alt="">
      </div>
    </div>

    <div class="group2">
      <ul>
        <li><a href="#">Home</a></li>
        <li><a href="#">Projects</a></li>
        <li><a href="#">About</a></li>
        <li><a href="#">Contact</a></li>
      </ul>
    </div>

    <div class="group3">
        <div class="hamburguer" @click="toggleMenu" :class="{hamburguer_active : x}"></div>
    </div>

    <ul class="group4" :class="{actived_navbar : x}">
      <li>
        <a href="#">Home</a>
      </li>
      <li>
        <a href="#">Projects</a>
      </li>
      <li>
        <a href="#">About</a>
      </li>
      <li>
        <a href="#">Contact</a>
      </li>
    </ul>

  </nav>
</template>

<script>
  export default{
    name: 'NavBar',
    components: {},
    data(){
      return {
        scrolled: false,
        x: false,
      }
    },
    methods:{
      toggleMenu(){
        this.x = !this.x;
      }
    },
    mounted(){
      window.document.onscroll = ()=>{
        if(window.scrollY > this.$refs.navbar.offsetTop){
          this.scrolled = true;
        }
        else{
          this.scrolled = false
        }
      }
    }
  }
</script>

<style scoped>
  #nav{
    width: 100vw;
    height: 90px;
    background-color: var(--black);
    position: relative;
    padding: 24px 60px;
    left: 0;
    top: 0;

    display: flex;
    justify-content: space-between;
    align-items: center;
    box-sizing: border-box;
    z-index: 10000;
    /* transition: all 600ms ease; */
  }

  .group1 .img-container{
    width: 90px;
    height: 50px;
  }

  .group1 .img-container img{
    width: 100%;
    height: 100%;
  }

  .group2{
    position: relative;
    right: 20px;
  }

  .group2 ul{
    display: flex;
    gap: 50px;
  }

  .group2 ul li a{
    color: var(--white);
  }

  .group3{
    display: none;
  }

  .hamburguer{
    width: 40px;
    height: 40px;
    position: relative;
    z-index: 900;
    cursor: pointer;
  }

  .hamburguer::after{
    content: '';
    position: absolute;
    top: 38%;
    left: 23%;
    width: 95%;
    height: 4%;
    background-color: #fff;
    transition: 1s ease;
  }

  .hamburguer::before{
    content: '';
    position: absolute;
    top: 63%;
    left: 63%;
    width: 55%;
    height: 4%;
    background-color: #fff ;
    transition: 1s ease;
  }

  .hamburguer_active{
        width: 40px;
        height: 40px;
        cursor: pointer;
    }
    
    .hamburguer_active::before{
        content: '';
        position: absolute;
    
        top: 50%;
        left: 23%;
    
        width: 55%;
        height: 10%;
        background-color: #fff;
        opacity: 0.8;
    
        transform: rotate(225deg);
    }
    
    .hamburguer_active::after{
        content: '';
        position: absolute;
    
        top: 50%;
        left: 23%;
    
        width: 55%;
        height: 10%;
        background-color: #fff;
        opacity: 0.8;
        transform: rotate(-405deg);
    }

 /*  #nav.sticky{
    position: fixed;
    padding: 20px 50px;
    backdrop-filter: blur(25px) saturate(144%);
    -webkit-backdrop-filter: blur(25px) saturate(144%);
    background-color: rgba(26, 26, 26, 0.51);
  } */

  .group4{
    width: 100vw;
    height: 100vh;
    position: fixed;
    top: 0;
    right: -1100px;
    background-color: black;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: 30px;
    transition: all 800ms ease;
  }

  .actived_navbar{
    right: 0;
  }

  .group4 li{
    padding: 24px 60px;
  }

  .group4 li a{
    display: inline-block;
    color: var(--white);
    width: 100%;
    height: 100%;
  }
  
  @media screen and (max-width: 900px){
    #nav{
      background-color: var(--red);
    }

    .group2{
      display: none;
    }

    .group3{
      display: block;
    }
  }
</style>