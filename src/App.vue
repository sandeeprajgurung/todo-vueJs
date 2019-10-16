<template>
  <div id="app">
     <Header />
    <router-view/>
  </div>
</template>

<script>
import Header from './components/layouts/Header.vue';
export default {
  name: "app",
  components: {
    Header
  }
}

</script>
<style>
  #app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
  }
  div {
      background-color: #f2f2f2;
  }
  h1 {
    font-size: 2.5em;
  }
  a {
    text-decoration: none;
  }
</style>
