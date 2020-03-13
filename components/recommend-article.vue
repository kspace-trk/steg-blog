<template>
  <div class="recommend" id="app">
    <div class="recommend-text-box">
      <p class="recommend-text">人気記事</p>
    </div>
    <div class="recommend-box">
      <div class="recommend-img">
        
      </div>
      <div class="article">
        <div class="articleTitle">
          {{ info.data.contents[0]["articleTitle"] }}
        </div>
        <div class="articleInfo">
          <div class="articleCategory">
            <p>{{ info.data.contents[0]["articleCategory"] }}</p>
          </div>
          <div class="articleDate"></div>
        </div>
        <div class="articleText">
          <p>こんにちは、僕です。今回はMacbook Pro 2015 を使って焼肉を焼いた際に起きた出来事について色々を書いていきたいと思います。場所は相模原の河原です。気温は18度と4月にしては暖かい気温でした。</p>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import axios from "axios";
import Vue from "vue";

export default {
  el: '#app',
  data() {
    return {
      info: null
    };
  },
  mounted() {
    axios
      .get("https://steg-blog.microcms.io/api/v1/article1", {
        headers: { "X-API-KEY": '86df9a31-91d6-4f0a-a022-1bd1ee558330' }
      })
      .then(response => {
          this.info = response
          console.log(this.info.data)
          console.log(this.info.data.contents[0]["articleTitle"])
      });
  }
}

</script>
<style>
.recommend {
  text-align: center;
}

.recommend-text {
  margin: auto;
  font-size: 1.5rem;
  width: 15%;
  color: #404040;
  border-bottom: solid 2px #707070;
}

.recommend-text-box {
  padding: 100px 0 70px 0;
}

.recommend-box {
  display: flex;
  margin: 0 120px 60px 120px;
}

.recommend-img {
  width: 70%;
  background-color: #404040;
}

.article {
  margin-left: 30px;
  text-align: left;
  width: 30%;
}
.articleTitle {
  font-size: 1.3rem;
  margin-top: 10px;
  border-bottom: solid 2px #707070;
}

.articleInfo {
  display: flex;
  margin-top: 15px;
}

.articleCategory {
  background-color: #20d8ba;
  border-radius: 5px;
}

.articleCategory p {
  color: #ffffff;
  font-size: 1rem;
  margin: 0 20px;
}

.articleDate {
  margin-left: 20px;
}

.articleDate p {
  font-size: 0.8rem;
}

.articleText {
  font-size: 0.8rem;
  margin-top: 30px;
}
</style>