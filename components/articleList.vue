<template>
    <div class="articleContents">
      <nuxt-link :to="'/articles/' + article.id">
      <img :src="article.image.url" alt="記事画像"  />
      <div class="articleCategory">
        <p>{{article.category}}</p>
      </div>
      <div class="articleContentsTitle">
        <p>{{article.title}}</p>
      </div>
      </nuxt-link>
    </div>
</template>

<script>

export default {
  props: ["article"]
};
</script>

<style>
.articleContents {
  width: 300px;
  margin: 0 auto;
  background-color: #ffffff;
  border-radius: 8px;
  margin-bottom: 50px;
  text-decoration: none;
}
.articleContents img {
  position: relative;
  width: 100%;
  height: 140px;
}
.articleContentsTitle {
  height: 60px;
  margin-bottom: 0;
  padding-left: 12px;
  padding-top: 10px;
}
.articleContentsTitle p{
  text-decoration: none;
  color: #282828;
}
.articleCategory {
  height: 16px;
  width: 35px;
  text-align: center;
}

.articleCategory p {
  font-size: 0.8rem;
}
</style>