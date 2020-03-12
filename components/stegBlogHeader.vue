<template>
    <div class="headerWrapper">
      <img src="~/assets/Steg-logo-white.png" alt="Steg Logo">
      <div class="headerSubIcon">
        <a href="https://github.com/project-steg" target="_blank"><img src="~/assets/GitHub-icon.png" alt="GitHub icon"></a>
        <a href="https://twitter.com/Steg_official" target="_blank"><img src="~/assets/twitter-icon.png" alt="Twitter icon"></a>
        <a href="https://team-steg.com/" target="_blank"><img src="~/assets/homepage-icon.png" alt="Homepage icon"></a>
      </div>
    </div>
</template>


<style>
.headerWrapper{
    height: 70px;
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

.headerSubIcon img{
  height: 40px;
  margin: auto 30px auto ;
  }
</style>