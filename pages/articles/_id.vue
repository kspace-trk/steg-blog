<template>
    <div class="contents">
      <stegBlogHeader />
      <contents :contents="item"/>
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
      item: data,
    };
  },
    components: {
    stegBlogHeader,
    contents,
  }
}
</script>

<style>

</style>

