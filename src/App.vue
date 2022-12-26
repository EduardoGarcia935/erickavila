<template>
  <div id="container">
    <HomeVue/>
    <ProjectsVue/>
    <AboutVue/>
    <ContactVue/>
  </div>
</template>

<script>
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
  }
}
</script>

<style scoped>
  #container{
    width: 100vw;
    min-width: 100vw;
    height: 100%;
  }
</style>
