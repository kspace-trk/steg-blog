<template>
    <div class="recommend container">
        <div class="recommend-text-box row">
            <p class="recommend-text col-xs-12 ">おすすめ記事</p>
        </div>
        <div class="recommend-box row">
            <div class="recommend-img col-md-6 col-xs-10">
                <img :src="recommend.image.url" alt="記事画像"  class="img-fluid" />
            </div>
            <div class="article col-md-6 col-xs-10">
                <div class="articleTitle">
                    <p>{{recommend.title}}</p>
                </div>
                <div class="articleInfo">
                    <div class="articleCategory">
                        <p>{{recommend.category}}</p>
                    </div>
                    <div class="articleDate">
                        <p>{{recommend.createdAt}}</p>
                    </div>
                </div>
                <div class="articleText">
                        <p>{{recommend.contents}}</p>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
import axios from "axios";
export default {
  props: ["recommend"]
};
</script>
<style>
.recommend{
    text-align: center;
}
.recommend-text{
    margin: auto;
    font-size: 1.5rem;
    color:#404040;
    border-bottom: solid 2px #707070;
}
.recommend-text-box{
    padding: 100px 0 70px 0;
}
.recommend-box{
    display: flex;
    margin: 0 0 60px 0;
}
.recommend-img{
}
.article{
    text-align: left;
}
.articleTitle{
    font-size: 1.3rem;
}
.articleInfo{
    display: flex;
}
.articleCategory{
    background-color: #20D8BA;
}
.articleCategory p{
    color: #FFFFFF;
    font-size: 1.0rem;
}
.articleDate p{
    font-size: 0.8rem;
}
.articleText{
    font-size: 0.8rem;
}
</style>