<template>
  <div class="article-list">
    <h6>最新文章</h6>
    <section>
      <article v-for="post in posts" :key="post.id" class="row list-body">
        <div class="col-12 col-md-5" v-if="post.hasCover">
          <img
            :src="post.cover"
            alt=""
            loading="lazy"
            class="img-fluid img-thumbnail"
          />
        </div>
        <div class="col-12 col-md-7">
          <header>{{ post.title }}</header>
          <p>{{ post.intro }}</p>
        </div>
      </article>
    </section>
  </div>
</template>

<script>
export default {
  name: "ArtcleList",
};
</script>