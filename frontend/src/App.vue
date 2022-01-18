<template>
  <div class="container-md">
    <div class="my-navbar">
      <Nav />
    </div>
    <div class="my-body">
      <router-view />
      <RightBar />
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import Nav from '@/components/Nav.vue'
import RightBar from '@/components/RightBar.vue'

export default {
  name:'App',
  components:{
    Nav,
    RightBar
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
}

</style>
