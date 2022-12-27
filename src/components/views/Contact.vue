<template>
  <div id="container">
    <h2 data-aos="fade-up" data-aos-duration="2000">Contact</h2>
  </div>
</template>

<script>
  export default{
    name: 'ContactVue',
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
    background-color: var(--red);
    color: var(--white);
    border-top: 1px solid white;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  h2{
    margin: 0 auto;
  }
</style>