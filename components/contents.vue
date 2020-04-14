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
  width: 80%;
  margin: 50px auto 80px;
}
.contents-title p{
  font-size: 2rem;
  color: #282828;
  font-family: 'M PLUS Rounded 1c', sans-serif;
  border-bottom:  solid 2px #E0E0E0;
  margin-bottom: 10px;
  padding-bottom: 5px;
}
.contents-img img{
    width: 100%;
    height: auto;
    margin-bottom: 30px;
}

.contents-text p{
  padding-bottom: 10px;
}
.contents-text img{
  width: 100%;
  height: auto;
}
.contents-text h1{
    font-size: 2rem;
    border-bottom: solid 2px #E0E0E0;
    margin: 10px 0 1.5rem 0;
    padding-bottom: 8px;
}
.contents-text h2{
    font-size: 1.5rem;
    border-bottom: solid 2px #E0E0E0;
    margin: 1.5rem 0 1.5rem 0;
    padding: 0 0 8px 13px;
    border-left: solid 5px #20d8ba;
}
.contents-text h3 {
    font-size: 1.25rem;
}
.contents-text ol {
    margin-left: 1rem;
}

</style>
