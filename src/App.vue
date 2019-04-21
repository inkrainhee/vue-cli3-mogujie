<template>
  <div id="app">
    <router-view/>
  </div>
</template>
<script>
export default {
  
}
</script>

<style lang="stylus">
*{
  margin 0;
  padding 0;
  box-sizing: border-box;
}

@font-face {
  font-family: 'iconfont';
  src: url('./assets/iconfonts/iconfont.eot');
  src: url('./assets/iconfonts/iconfont.eot?#iefix') format('embedded-opentype'),
      url('./assets/iconfonts/iconfont.woff2') format('woff2'),
      url('./assets/iconfonts/iconfont.woff') format('woff'),
      url('./assets/iconfonts/iconfont.ttf') format('truetype'),
      url('./assets/iconfonts/iconfont.svg#iconfont') format('svg');
}
.iconfont{
    font-family:"iconfont" !important;
    font-size:16px;font-style:normal;
    -webkit-font-smoothing: antialiased;
    -webkit-text-stroke-width: 0.2px;
    -moz-osx-font-smoothing: grayscale;
}

</style>
