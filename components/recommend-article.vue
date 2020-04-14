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
        <div class="article-title">
          <nuxt-link :to="'/articles/' + recommend.id" tag="p">
            <p>{{recommend.title}}</p>
          </nuxt-link>
        </div>
        <div class="article-info">
          <div class="article-category">
            <p>{{recommend.category}}</p>
          </div>
          <div class="article-date">
            <p>{{recommend.createdAt}}</p>
          </div>
        </div>
        <div class="article-text"  v-html="$md.render(recommend.contents)">
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
.recommend-img{
  filter: drop-shadow(5px 5px 10px rgba(0,0,0,0.3));
}
.article {
  text-align: left;
}
.article-title p{
  font-size: 1.3rem;
  color: #282828;
  text-decoration: none;
  cursor: pointer;
}
.article-info {
  display: flex;
}
.article-category {
  text-align: center;
  line-height: 1.3;
}
.article-category p {
  color: #ffffff;
  font-size: 0.8rem;
  background-color: #20d8ba;
  
}
.article-date p {
  font-size: 0.8rem;
  line-height: 1.3;
}
.article-text {
  max-width: 400px;
  max-height: 160px;
  font-size: 0.8rem;
  overflow: hidden;
  color: #505050;
}

.article-text h1 {
  font-size: 0.8rem;
}
.article-text h2 {
  font-size: 0.8rem;
}
.article-text h3 {
  font-size: 0.8rem;
}
</style>