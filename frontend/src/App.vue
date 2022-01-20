<template>
  <div class="container-md my-con">
    <div class="my-navbar">
      <Nav />
    </div>
    <div class="my-body row">
      <router-view class="col-md-8 col-12" />
      <RightBar class="col-md-4 col-12" />
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
.my-con{
  padding-top: 3rem;
}
.my-body{
  padding: 15px;
}
</style>

<style scoped>

</style>