<template>
<div id="app">
    <div class="articleListFlex">
        <div class="articleContents">
            <img src="~assets/img/article-img.png" alt="記事画像" width="270px" height="140px">
            <div class="articleContentsTitle">
                <div class="articleCategory">
                    <p>PHP</p>
                </div>
                <p>{{info}}</p>
            </div>
        </div>
    </div>
</div>
</template>

<script>
import Vue from 'vue'
import axios from 'axios'

export default {
   name:'app',
    
    data(){
        return{
            info:null
        }
    },
    mounted() {
        axios.get('https://steg-blog.microcms.io/api/v1/article1/',{
            headers: {'X-API-KEY': '86df9a31-91d6-4f0a-a022-1bd1ee558330'}
    })
    .then(response => {
        console.log('できたあああああああ')
        (this.info = response.articleList)
    })
    .catch(error => {
        console.log('できないいいいいいいい')
    })
  }
}

</script>

<style>
.articleListFlex{
    margin: 60px 15em 100px 15em;
    padding-bottom: 60px;
    display: flex;
    justify-content: space-evenly;
    flex-wrap: wrap;
}

.articleContents{
    width: 270px;
    height: 210px;
    background-color: #ffffff;
    margin: 0 0.2em 20px 0.2em;
    display: block;
    justify-content: center;
    border-radius: 8px;
}
.articleContentsTitle{
    height: 60px;
    margin-bottom: 0;
    padding-left: 12px;
    padding-top: 10px;
}
.articleCategory{
    height: 60;
    width: 35px;
    text-align: center;
}

.articleCategory p{
    font-size: 0.8rem;
}
</style>