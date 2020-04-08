<template>
    <div class="contents-wrapper">
      <div class="contents-title">
        <h1>{{contents.title}}</h1>
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
.contents-title h1{
  font-size: 30px;
  color: #282828;
  font-family: 'M PLUS Rounded 1c', sans-serif;
  border-bottom:  solid 1px #707070;
  padding-bottom: 5px;
}
</style>
