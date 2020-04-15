<template>
  <nuxt-link :to="'/articles/' + article.id" tag="div" class="article-contents">
    <img :src="article.image.url" alt="記事画像" />
    <div class="article-category">
      <p>{{article.category}}</p>
    </div>
    <div class="article-contents-title">
      <p>{{article.title}}</p>
    </div>
  </nuxt-link>
</template>

<script>
export default {
  props: ["article"]
};
</script>

<style>
.article-contents {
  width: 300px;
  height: 220px;
  background-color: #ffffff;
  border-radius: 8px;
  margin-bottom: 50px;
  text-decoration: none;
  filter: drop-shadow(5px 5px 10px rgba(0,0,0,0.3));
  cursor: pointer;
}
.article-contents img {
  position: relative;
  width: 100%;
  height: 140px;
}
.article-contents-title {
  height: 60px;
  margin-bottom: 0;
  padding-left: 12px;
  padding-top: 10px;
}
.article-contents-title p {
  text-decoration: none;
  color: #282828;
}
.article-category {
  width: 50px;
  text-align: center;
  line-height: 1.4;
}

.article-category p {
  font-size: 0.8rem;
  color: #ffffff;
  background-color: #20d8ba;
  border-radius: 4px;
}
</style>