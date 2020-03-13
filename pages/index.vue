<template>
<div class="index">
  <stegBlogHeader />
    <div class="mainVisual">
      <img src="~assets/img/steg-circle-icon.png" alt="circle icon">
    </div>
    <recommended-article />
    
  </div>
</template>

<script>

import stegBlogHeader from '@/components/stegBlogHeader.vue'
export default {
  data() {
    return {
    }
  },
  components: {
    stegBlogHeader,
  },
  methods: {
  },
  mounted() {
  }
}
</script>

<style>
.mainVisual{
  background-image: url('~assets/img/main-visual.jpg');
  height: 400px;
  background-size: cover;
  background-position: center;
  width: 100vw;
  justify-content: center;
  display: flex;
  align-items: center;
}

.mainVisual img{
}
</style>