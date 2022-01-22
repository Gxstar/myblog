<template>
  <div class="home">
    <h6>最新文章</h6>
    <section>
      <article v-for="post in posts" :key="post.id">
        <header>{{ post.title }}</header>
        <img :src="post.cover" alt="" srcset="">
        <p>{{ post.intro }}</p>
        <hr>
      </article>
    </section>
  </div>
</template>

<script>
// @ is an alias to /src
// import Nav from '@/components/Nav.vue'

export default {
  name: 'Home',
  components: {

  },
  data(){
    return {
      posts:[
        {
          id:1,
          title:"第一篇文章",
          cover:"https://gxstar123.cn/wp-content/uploads/2022/01/%E5%BE%AE%E4%BF%A1%E5%9B%BE%E7%89%87_20220121225908-769x469.jpg",
          intro:"这是第一篇文章的简介",
          text:"这是第一篇文章的简介,大沙发斯蒂芬卡世纪东方卡视角东方红卡闪电发货尅五花肉饭度搜阿福卡拉时代峻峰虎课网哈人防守打法可好看"
        },
        {
          id:2,
          title:"第二篇文章",
          cover:"https://gxstar123.cn/wp-content/uploads/2022/01/%E5%BE%AE%E4%BF%A1%E5%9B%BE%E7%89%87_20220121225908-769x469.jpg",
          intro:"这是第二篇文章的简介",
          text:"这是第二篇文章的简介,大沙发斯蒂芬卡世纪东方卡视角东方红卡闪电发货尅五花肉饭度搜阿福卡拉时代峻峰虎课网哈人防守打法可好看"
        }
      ]
    };
  }
}
</script>
