<template>
    <div id="home">
        <home-header>
          <template v-slot:header>
            <div class="search-bar" :class="showPage==2?'':'phone-search-bar'">
              <span class="icon-sort" v-if="showPage==2">
                
              </span>
              <span class="icon-sort-box">
                <i class="iconfont icon-sort-phone" v-if="showPage==1">&#xeba1;</i>  
                <span class="txt-sort-phone" v-if="showPage==1">分类</span>              
              </span>
              
            
              <div class="search">
                <input id="search-form-input" :class="showPage==2?'':'phone-search-item'" class="search-item"  type="text" name="q" placeholder="背带裤" data-query-word="背带裤">
              </div>
              <span class="icon-news" v-if="showPage==2">
                
              </span>
              <span class="icon-camara" v-if="showPage==1">
                
              </span>
            </div>
              
          </template>
        </home-header>
    </div>
</template>

<script>
import HomeHeader from '../components/base/Header.vue'
export default {
    components:{
      HomeHeader
    },
    name:'home',
    data(){
      return {
        showPage : 3
      }
    },
    created(){
      if((navigator.userAgent.match(/(iPhone|iPod|Android|ios)/i))){

        //移动端
        this.showPage=1
      }else{
        this.showPage=2
      }
    }
}
</script>

<style lang="stylus" scoped>
.search-bar
  display flex
  position absolute
  top 0
  width 100%
  height 0.92rem
  padding 0.15rem 0.1rem
  background-color #fff
  border-bottom 1px solid #e5e5e5
  z-index 100
  overflow hidden
  span.icon-sort
    text-align center
    display inline-block
    width 1rem
    height 100%
    font-size 0.6rem
    background-image: url('../assets/icon/icon-sort.png')
    background-repeat: no-repeat;
    background-position center
    background-size: 0.44rem auto;
    
  div.search
    -webkit-flex: 1;
    -webkit-box-flex: 1;
    width auto 
    input.search-item
      display: block;
      width: 100%;
      padding-left: 0.6rem;
      height: 0.6rem;
      font-size: 0.24rem;
      color: #999;
      border: none;
      background-image: url('../assets/icon/icon-search.png');
      background-color #eee
      background-repeat: no-repeat;
      background-position left 0.15rem center
      background-size: 0.35rem;
      border-radius: 0.1rem;
  span.icon-news
    text-align center
    display inline-block
    width 1rem
    height 100%
    font-size 0.6rem
    background-image: url('../assets/icon/icon-news.png')
    background-repeat: no-repeat;
    background-position center
    background-size: 0.44rem auto;
    color #666
  span.icon-camara
    text-align center
    display inline-block
    position absolute
    right -3px 
    top 0
    width 1rem
    height 100%
    font-size 0.6rem
    background-image: url('../assets/icon/icon-news.png')
    background-repeat: no-repeat;
    background-position center
    background-size: 0.44rem auto;
    color #666
  .phone-search-item
    border-radius: 4rem !important;
    background-color #fff !important;
  span.icon-sort-box
    display inline-block
    height 100%
    i.icon-sort-phone
      text-align center
      display block
      width 1rem
      height 100%
      font-size 0.4rem
      color:#fff
    span.txt-sort-phone
      z-index:200

.phone-search-bar
  background-color #ff5777 !important;
</style>

