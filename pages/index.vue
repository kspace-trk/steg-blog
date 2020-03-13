<template>
<div class="index">
  <stegBlogHeader />
    <div class="mainVisual">
      <img src="~assets/img/steg-circle-icon.png" alt="circle icon">
    </div>
    <recommend-article />
    <articleList />
  </div>
</template>

<script>
import Vue from 'vue'
import stegBlogHeader from '@/components/stegBlogHeader.vue'
import RecommendArticle from '@/components/recommend-article.vue'
import articleList from '@/components/articleList.vue'

export default {
  data() {
    return {
    }
  },
  components: {
    stegBlogHeader,
    RecommendArticle,
    articleList
  },
  methods: {
  },
  mounted() {
  }
}
</script>

<style>
.index{
  background-color: #f7f7f7;
}
.mainVisual{
  background-image: url('~assets/img/main-visual.jpg');
  height: 400px;
  background-size: cover;
  background-position: center;
  width: 100%;
  justify-content: center;
  display: flex;
  align-items: center;
}

.mainVisual img{
}

</style>