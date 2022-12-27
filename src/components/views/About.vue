<template>
  <div id="container">
    <h2 data-aos="fade-left" data-aos-duration="2000">About</h2>
  </div>
</template>

<script>
  export default{
    name: 'AboutVue',
    components: {},
    data(){
      return{

      }
    },
  }
</script>

<style scoped>
  #container{
    width: 100vw;
    min-width: 100vw;
    height: 100vh;
    min-height: 100vh;
    background-color: var(--black);
    color: var(--white);
    border-top: 1px solid white;
    display: flex;
    justify-content: center;
    align-items: center;
  }
</style>