
<template>
  <!-- <Header></Header> -->
  <!-- <Home /> -->
  <router-view />
  <!-- <test></test> -->

</template>

<script>
// import test from './components/test.vue'
// import Home from './components/Home.vue'
// import Header from './components/Header.vue'
import '@fortawesome/fontawesome-free/css/all.min.css'
export default {
  name: 'App',
  components: {
    // Header
    // test
  }
}
</script>

<style>
@import "https://cdn.jsdelivr.net/npm/bulma@0.9.4/css/bulma.min.css";
@import url('https://fonts.googleapis.com/css2?family=Euphoria+Script&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Mali:wght@500&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Tilt+Neon&display=swap');

#app {
  /* font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  /* color: #2c3e50; */
  user-select: none;


}
#logo {
    font-size: 50px;
    font-family: 'Euphoria Script', cursive;
}
#mali{
  font-family: 'Mali', cursive;
}

#euphoria{
  font-family: 'Euphoria Script', cursive;
}

#tilt{
  font-family: 'Tilt Neon', cursive;
}
</style>


