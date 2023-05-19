<template>
  <navbar></navbar>
  <router-view></router-view>
</template>

<script>
  import Navbar from './components/Navbar.vue';

  export default {
    components: {
      Navbar
    }
  }
</script>

<style lang="scss">
  @import './assets/scss/mixins';

  @font-face {
    font-family: 'Public Sans Regular';
    src: url('./assets/fonts/PublicSans-Regular.ttf');
    font-weight: 400;
  }

  :root {
    --dark-blue: #2d314d;
    --lime-green: #31d35c;
    --bright-cyan: #2bb7da;
    --grayish-blue: #9698a6;
    --light-grayish-blue: #f2f3f5;
    --very-light-gray: #fafafa;
  }
  
  * {
    padding: 0;
    margin: 0;
    box-sizing: border-box;
    font-family: 'Public Sans Regular', sans-serif;
    color: var(--dark-blue);
  }

  body {
    background-color: var(--very-light-gray);
    
    /* & > * {
      padding: 0 8rem;
    } */
  }

  h1 {
    font-size: 54.93px;
  }

  h2 {
    font-size: 43.95px;
  }

  h3 {
    font-size: 35.16px;
  }

  h4 {
    font-size: 28.13px;
  }

  h5 {
    font-size: 22.50px;
  }

</style>