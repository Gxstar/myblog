<template>
  <div class="home">
    
  </div>
</template>

<script>
// @ is an alias to /src
// import Nav from '@/components/Nav.vue'

export default {
  name: "Home",
  components: {},
  data() {
    return {
      posts: [
        {
          id: 1,
          title: "第一篇文章",
          cover:
            "https://s1.ax1x.com/2020/10/06/0UwokV.md.jpg",
          intro: "这是第一篇文章的简介",
          text: "这是第一篇文章的简介,大沙发斯蒂芬卡世纪东方卡视角东方红卡闪电发货尅五花肉饭度搜阿福卡拉时代峻峰虎课网哈人防守打法可好看",
          hasCover: true,
        },
        {
          id: 2,
          title: "第二篇文章",
          cover:
            "https://s1.ax1x.com/2020/10/06/0Uw5T0.md.jpg",
          intro: "这是第二篇文章的简介",
          text: "这是第二篇文章的简介,大沙发斯蒂芬卡世纪东方卡视角东方红卡闪电发货尅五花肉饭度搜阿福卡拉时代峻峰虎课网哈人防守打法可好看",
          hasCover: false,
        },
      ],
    };
  },
};
</script>

<style scoped>
.list-body{
  padding: 15px 25px 15px 5px;
}
.list-body::after{
  content:'';
  width:100%;
  height:1px;
  background-color: lightgray;
  position: relative;
  top: 1.5rem;
}
</style>