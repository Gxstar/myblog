<template>
  <div class="home">
    <ArtilceList :list_type="type" />
  </div>
</template>

<script>
// @ is an alias to /src
// import Nav from '@/components/Nav.vue'
import ArtilceList from "../components/ArtilceList.vue";

export default {
  name: "Home",
  components: { ArtilceList },
  data(){
    return {
      type:"最新文章"
    }
  },
};
</script>

<style scoped>

</style>