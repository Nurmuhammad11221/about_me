<template>
    <Nav />
    <Header />
    <Konikmalar />
    <Main />
    <Web />
    <Game />
    <Footer /> 
  </template>
  
  <script>
  import Nav from './components/Nav.vue';
  import Header from './components/Header.vue';
  import Main from './components/Main.vue';
  import Footer from './components/Footer.vue';
  import Konikmalar from './components/Konikmalar.vue';
  import Game from './components/Game.vue';
  import Web from './components/Web.vue'; 
  
  
  export default {
    components: {
      Nav,
      Header,
      Konikmalar,
      Main,
      Footer,
      Game,
      Web
      
    },
  };
  </script>
  
<style>
    *{
      padding: 0;
      margin: 0;
      text-decoration: none;
    }

    body, html {
      margin: 0;
      padding: 0;
      height: 100%;
      display: flex;
      flex-direction: column;
  }

  /* Asosiy App konteyneri */
  .app {
      display: flex;
      flex-direction: column;
      min-height: 100vh;
  }

  .app > *:first-child {
      flex: 1;
  } 
  
</style>


