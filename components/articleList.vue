<template>
    <div class="articleListFlex">
        <div class="articleContents">
            <img src="~assets/img/article-img.png" alt="記事画像" width="270px" height="140px">
            <div class="articleContentsText">
                <p>PHP</p>
                <p>PHPでHello World出力してみた</p>
            </div>
        </div>
    </div>
</template>

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
.articleContentsText{
    height: 60px;
    margin-bottom: 0;
}
</style>