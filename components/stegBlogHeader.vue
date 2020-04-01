<template>
    <div class="headerWrapper">
      <img src="~/assets/img/Steg-logo-white.png" alt="Steg Logo">
      <div class="headerSubIcon">
        <a href="https://github.com/project-steg" target="_blank"><img src="~/assets/img/GitHub-icon.png" alt="GitHub icon"></a>
        <a href="https://twitter.com/Steg_official" target="_blank"><img src="~/assets/img/twitter-icon.png" alt="Twitter icon"></a>
        <a href="https://team-steg.com/" target="_blank"><img src="~/assets/img/homepage-icon.png" alt="Homepage icon"></a>
      </div>
    </div>
</template>


<style>
.headerWrapper{
    height: 65px;
    width: 100%;
    background-color: #404040;
    z-index: 100;
    display: flex;
    align-items: center;
}

.headerWrapper img{
  position: relative;
  height: 80%;
  margin: auto auto auto 30px;
}

.headerSubIcon{
  margin-right: 10px;
}

.headerSubIcon img{
  height: 30px;
  margin: auto 25px auto ;
  }
</style>