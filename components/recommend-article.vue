<template>
  <div v-if="recommend.recommend" class="recommend container">
    <div class="recommend-text-box row">
      <p class="recommend-text col-xs-12">人気記事</p>
    </div>
    <div class="recommend-box row">
      <div class="recommend-img col-md-6 col-xs-10">
        <nuxt-link :to="'/articles/' + recommend.id">
          <img :src="recommend.image.url" alt="記事画像" class="img-fluid" />
        </nuxt-link>
      </div>

      <div class="article col-md-6 col-xs-10">
        <div class="articleTitle">
          <nuxt-link :to="'/articles/' + recommend.id">
            <p>{{recommend.title}}</p>
          </nuxt-link>
        </div>
        <div class="articleInfo">
          <div class="articleCategory">
            <p>{{recommend.category}}</p>
          </div>
          <div class="articleDate">
            <p>{{recommend.createdAt}}</p>
          </div>
        </div>
        <div class="articleText"  v-html="$md.render(recommend.contents)">
          <p>{{recommend.contents}}</p>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  props: ["recommend"],
  mounted(){
    console.log(this.recommend.contents)
  },
};
</script>
<style>
.recommend {
  text-align: center;
}
.recommend-text {
  margin: auto;
  font-size: 1.5rem;
  color: #404040;
  font-weight: 700;
  border-bottom: solid 2px #707070;
}
.recommend-text-box {
  padding: 100px 0 70px 0;
}
.recommend-box {
  display: flex;
  margin: 0 0 60px 0;
}

.article {
  text-align: left;
}
.articleTitle a{
  font-size: 1.3rem;
  color: #282828;
  text-decoration: none;
}
.articleInfo {
  display: flex;
}
.articleCategory {
  background-color: #20d8ba;
}
.articleCategory p {
  color: #ffffff;
  font-size: 1rem;
}
.articleDate p {
  font-size: 0.8rem;
}
.articleText {
  max-width: 400px;
  max-height: 160px;
  font-size: 0.8rem;
  overflow: hidden;
  color: #505050;
}

.articleText h1 {
  font-size: 0.8rem;
}
.articleText h2 {
  font-size: 0.8rem;
}
.articleText h3 {
  font-size: 0.8rem;
}
</style>