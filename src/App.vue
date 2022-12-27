<template>
  <div id="container">
    <nav ref="navbar" id="nav">
      <div class="group1" data-aos="fade-up" data-aos-duration="1200" data-aos-delay="100">
        <div class="img-container">
          <img src="./assets/images/logo.png" alt="">
        </div>
      </div>
      <div class="group2">
        <ul>
          <li data-aos="fade-up" data-aos-duration="1200" data-aos-delay="300"><a href="#home" >Home</a></li>
          <li data-aos="fade-up" data-aos-duration="1200" data-aos-delay="500"><a href="#projects" >Projects</a></li>
          <li data-aos="fade-up" data-aos-duration="1200" data-aos-delay="700"><a href="#about" >About</a></li>
          <li data-aos="fade-up" data-aos-duration="1200" data-aos-delay="900"><a href="#contact" >Contact</a></li>
        </ul>
      </div>
      <div class="group3">
          <div class="hamburguer" @click="toggleMenu" :class="{hamburguer_active : x}"></div>
      </div>
      <ul class="group4" :class="{actived_navbar : x}">
        <li>
          <a href="#home">Home</a>
        </li>
        <li>
          <a href="#projects">Projects</a>
        </li>
        <li>
          <a href="#about">About</a>
        </li>
        <li>
          <a href="#contact">Contact</a>
        </li>
      </ul>
    </nav>
    <div id="home">
      <HomeVue/>
    </div>
    <div id="projects">
      <ProjectsVue/>
    </div>
    <div id="about">
      <AboutVue/>
    </div>
    <div id="contact">
      <ContactVue/>
    </div>
  </div>
</template>

<script>
import HomeVue from './components/views/Home.vue';
import ProjectsVue from './components/views/Projects.vue';
import AboutVue from './components/views/About.vue';
import ContactVue from './components/views/Contact.vue';

import "./assets/styles/navBar.css"

export default {
  name: 'App',
  components: {
    HomeVue,
    ProjectsVue,
    AboutVue,
    ContactVue,
  },
  data(){
    return {
      x: false,
    }
  },
  methods: {
    toggleMenu(){
      this.x = !this.x;
    }
  }
}
</script>

<style scoped>
  #container{
    overflow-x: hidden;
  }
</style>
