<template>
    <div class="recommend">
        <div class="recommend-text-box">
            <p class="recommend-text">人気記事</p>
        </div>
        <div class="recommend-box">
            <div class="recommend-img">

            </div>
            <div class="article">
                <p>記事を書きましょう</p>
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
    text-align: center;
    width: 30%;
}
</style>