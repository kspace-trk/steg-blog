<template>
  <div class="index">
    <stegBlogHeader />
    <div class="mainVisual">
      <img src="~assets/img/steg-circle-icon.png" alt="circle icon" />
    </div>
    <div v-for="elem in item" :key="elem.id">
    <recommend-article :recommend="elem" />
    </div>
    <b-container>
      <div class="recommend-text-box row">
      <p class="recommend-text col-xs-12">記事一覧</p>
    </div>
      <b-row class="article-list">
        <b-col lg="4" md="6" sm="8" v-for="elem in item" :key="elem.id" class="article-list">
          <articleList :article="elem" />
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script>
import axios from "axios";
import stegBlogHeader from "@/components/stegBlogHeader.vue";
import RecommendArticle from "@/components/recommend-article.vue";
import articleList from "@/components/articleList.vue";

export default {
  data() {
    return {
      item: []
    };
  },
  async asyncData() {
    const { data } = await axios.get(
      "https://steg-blog.microcms.io/api/v1/article",
      {
        headers: { "X-API-KEY": "86df9a31-91d6-4f0a-a022-1bd1ee558330" }
      }
    );
    
    return {
      item: data.contents
    };
  },

  components: {
    stegBlogHeader,
    RecommendArticle,
    articleList
  }
};
</script>

<style>
.index {
  background-color: #f7f7f7;
}
.mainVisual {
  background-image: url("~assets/img/main-visual.jpg");
  height: 400px;
  background-size: cover;
  background-position: center;
  width: 100%;
  justify-content: center;
  display: flex;
  align-items: center;
}

</style>