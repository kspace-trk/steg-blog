<template>
    <div class="recommend">
        <div class="recommend-text-box">
            <p class="recommend-text">人気記事</p>
        </div>
        <div class="recommend-box">
            <div class="recommend-img">

            </div>
            <div class="article">
                <div class="articleTitle">
                    <p>PHPでHello World出力してみた</p>
                </div>
                <div class="articleInfo">
                    <div class="articleCategory">
                        <p>PHP</p>
                    </div>
                    <div class="articleDate">
                        <p>3/10 19:40</p>
                    </div>
                </div>
                <div class="articleText">
                        <p>こんにちは、僕です。今回はMacbook Pro 2015 を使って焼肉を焼いた際に起きた出来事について色々を書いていきたいと思います。場所は相模原の河原です。気温は18度と4月にしては暖かい気温でした。</p>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    
}
</script>
<style>
.recommend{
    text-align: center;
}

.recommend-text{
    margin: auto;
    font-size: 1.5rem;
    width: 15%;
    color:#404040;
    border-bottom: solid 2px #707070;
}

.recommend-text-box{
    padding: 100px 0 70px 0;
}

.recommend-box{
    display: flex;
    margin: 0 120px 60px 120px;

}

.recommend-img{
    background-color: #707070;
    width: 70%;
    height: 300px;
}

.article{
    margin-left: 30px;
    text-align: left;
    width: 30%;
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