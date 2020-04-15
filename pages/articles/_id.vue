<template>
  <div class="contents">
    <stegBlogHeader />
    <b-container>
      <div class="articleContents">
        <contents :contents="item" />
      </div>
    </b-container>
  </div>
</template>

<script>
import axios from "axios";
import stegBlogHeader from "@/components/stegBlogHeader.vue";
import contents from "@/components/contents.vue";
export default {
  data() {
    return {
      item: []
    };
  },
  async asyncData({ params }) {
    const { data } = await axios.get(
      `https://steg-blog.microcms.io/api/v1/article/${params.id}`,
      {
        headers: { "X-API-KEY": "86df9a31-91d6-4f0a-a022-1bd1ee558330" }
      }
    );
    return {
      item: data
    };
  },
  components: {
    stegBlogHeader,
    contents
  }
};
</script>

<style>
.contents {
  background-image: url("~@/assets/img/article-background.jpg");
  background-size: cover;
  background-attachment: fixed;
}
.articleContents {
  border-radius: 20px;
  margin: 50px auto;
  width: 90%;
  height: auto;
  background-color: #ffffff;
  padding-top: 30px;
}
</style>

