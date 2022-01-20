<template>
  <div class="main-body">
    <nav class="navbar navbar-expand-md navbar-light">
      <div class="container-fluid">
        <a class="navbar-brand" href="#">阿星的小站</a>
        <button
          class="navbar-toggler"
          type="button"
          data-bs-toggle="collapse"
          data-bs-target="#navbarNavAltMarkup"
          aria-controls="navbarNavAltMarkup"
          aria-expanded="false"
          aria-label="Toggle navigation"
        >
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNavAltMarkup">
          <div class="navbar-nav">
            <router-link class="nav-link" :to="'/'"
              >首页</router-link
            >
            <router-link
              v-for="cat in cats"
              :key="cat.id"
              class="nav-link"
              :to="'/cats/' + cat.id"
              >{{ cat.name }}</router-link
            >
            <router-link class="nav-link" :to="'/about'">关于</router-link>
          </div>
        </div>
      </div>
    </nav>
  </div>
</template>

<script>
export default {
  name: "Nav",
  props: {},
  data() {
    return {
      cats: [
        { id: 1, name: "学习笔记" },
        { id: 2, name: "所想所感" },
      ],
    };
  },
};
</script>

<style scoped>
</style>