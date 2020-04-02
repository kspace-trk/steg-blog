<template>
    <div class="articleContents">
      <img :src="article.articleImg.url" alt="記事画像" />
      <div class="articleCategory">
        <p>{{article.articleCategory}}</p>
      </div>
      <div class="articleContentsTitle">
        <p>{{article.articleTitle}}</p>
      </div>
    </div>
</template>

<script>
import axios from "axios";

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
.articleCategory {
  height: 16px;
  width: 35px;
  text-align: center;
}

.articleCategory p {
  font-size: 0.8rem;
}
</style>