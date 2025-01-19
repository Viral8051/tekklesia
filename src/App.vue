<template>
  <div id="app">
    <loader/>
  </div>
</template>

<script>


import loader from './components/loader'



export default {
  
  name: 'App',
  components: {
    loader,
  }
}
</script>

<style>
@import url('./assets/style.css');
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  
}
*{
  font-family: "Monserrat";
  font-style: normal;
  font-weight: 400;
}
a{
  text-decoration: none;
}

@import url(./assets/style.css);
</style>
