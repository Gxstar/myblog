<template>
  <div class="article-list">
    <h6>{{list_type}}</h6>
    <section>
      <article v-for="post in posts" :key="post.id" class="row list-body">
        <div class="col-12 col-md-5" v-if="post.hasCover">
          <img
            :src="post.cover"
            alt=""
            loading="lazy"
            class="img-thumbnail"
          />
        </div>
        <div class="col-12 col-md-7">
          <header><h5>{{ post.title }}</h5></header>
          <p class="fs-6 fw-light my-text-cut">{{ post.text }}</p>
        </div>
      </article>
    </section>
  </div>
</template>

<script>
export default {
  name: "ArtcleList",
  props:["list_type"],
  data() {
    return {
      posts: [
        {
          id: 1,
          title: "第一篇文章",
          cover:
            "https://s1.ax1x.com/2020/10/06/0UwokV.md.jpg",
          intro: "这是第一篇文章的简介",
          text: "这是第一篇文章的简介,大沙发斯蒂芬卡世纪东方卡视角东方红卡闪电发货尅五花肉饭度搜阿福卡拉时卡世纪东方监控室打开了好久考试好地方健康函数肯定会反馈按时到付款杀毒发货卡萨打开了付好款交电话费开始还得看返回按时肯定会分开始的覅伙委会我如花生放看都好看发hi阿尔哈看回放斯卡迪是代峻峰虎课网哈人防守打法可好看adfasdf发电房三级啊是假的傅雷家书大浪费静安寺肯德基富士康的卡萨丁",
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
  letter-spacing: 1.25px;
}
.list-body::after{
  content:'';
  width:100%;
  height:1px;
  background-color: lightgray;
  position: relative;
  top: 1.5rem;
}
.my-text-cut{
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-line-clamp: 7;
  overflow: hidden;
}
</style>