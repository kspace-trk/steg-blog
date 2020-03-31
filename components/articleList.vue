<template>
  <div id="app">
    <div class="articleListFlex">
      <div class="articleContents">
        <img :src="article.articleImg.url" alt="記事画像" />
        <div class="articleCategory">
          <p>{{article.articleCategory}}</p>
        </div>
        <div class="articleContentsTitle">
          <p>{{article.articleTitle}}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios";

export default {
  props:["article"],
};

</script>

<style>
.articleListFlex {
  margin: 60px 15em 100px 15em;
  padding-bottom: 60px;
  display: flex;
  justify-content: space-evenly;
  flex-wrap: wrap;
}

.articleContents {
  width: 270px;
  height: 210px;
  background-color: #ffffff;
  margin: 0 0.2em 20px 0.2em;
  display: block;
  justify-content: center;
  border-radius: 8px;
}
.articleContents img {
  width: 270px;
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