<template>
    <div class="contents-wrapper">
      <div class="contents-title">
        <p>{{contents.title}}</p>
      </div>
      <div class="contents-img">
          <img :src="contents.image.url" alt="記事画像"  />
      </div>
      <div class="contents-text" v-html="$md.render(contents.contents)">
      </div>
    </div>
</template>
<script>
export default {
    props: ["contents"]
}
</script>
<style>
@import url('https://fonts.googleapis.com/css2?family=M+PLUS+Rounded+1c&display=swap');
.contents-wrapper{
  width: 700px;
  margin: 100px auto 0;
}
.contents-title p{
  font-size: 2rem;
  color: #282828;
  font-family: 'M PLUS Rounded 1c', sans-serif;
  border-bottom:  solid 1px #707070;
  padding-bottom: 5px;
}
.contents-img img{
    width: 100%;
    margin-bottom: 30px;
}
h1{
    font-size: 2rem;
    border-bottom: solid 1px #707070;
    margin-bottom: 1.5rem;
}
h2{
    font-size: 1.5rem;
    border-bottom: solid 1px #707070;
    margin-bottom: 1.5rem;
}
h3 {
    font-size: 1.25rem;
}
</style>
