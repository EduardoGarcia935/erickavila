<template>
  <div id="container">
    <NavBar/>
    <HomeVue/>
    <ProjectsVue/>
    <AboutVue/>
    <ContactVue/>
  </div>
</template>

<script>
import NavBar from './components/elements/NavBar.vue';
import HomeVue from './components/views/Home.vue';
import ProjectsVue from './components/views/Projects.vue';
import AboutVue from './components/views/About.vue';
import ContactVue from './components/views/Contact.vue';

export default {
  name: 'App',
  components: {
    HomeVue,
    ProjectsVue,
    AboutVue,
    ContactVue,
    NavBar
}
}
</script>

<style scoped>
  #container{
    overflow-x: hidden;
  }
</style>
