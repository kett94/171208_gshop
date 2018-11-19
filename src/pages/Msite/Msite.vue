<template>
  <section class="miste">
    <!--首页头部-->
    <HeaderTop title="福建省龙岩市">
      <span class="header_search" slot="search">
        <i class="iconfont icon-sousuo"></i>
      </span>
      <span class="header_login" slot="login">
        <span class="header_login_text">登录|注册</span>
      </span>
    </HeaderTop>
    <!--首页导航-->
    <nav class="msite_nav">
      <div class="swiper-container">
        <div class="swiper-wrapper">
          <div class="swiper-slide">
            <a href="javascript:" class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/1.jpg" alt="">
              </div>
              <span>甜品饮品</span>
            </a>
            <a href="javascript:" class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/2.jpg" alt="">
              </div>
              <span>商超遍历</span>
            </a>
            <a href="javascript:" class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/3.jpg" alt="">
              </div>
              <span>美食</span>
            </a>
            <a href="javascript:" class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/4.jpg" alt="">
              </div>
              <span>简餐</span>
            </a>
            <a href="javascript:" class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/5.jpg" alt="">
              </div>
              <span>新店特惠</span>
            </a>
            <a href="javascript:" class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/6.jpg" alt="">
              </div>
              <span>准时达</span>
            </a>
            <a href="javascript:" class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/7.jpg" alt="">
              </div>
              <span>预定早餐</span>
            </a>
            <a href="javascript:" class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/8.jpg" alt="">
              </div>
              <span>土豪推荐</span>
            </a>
          </div>
          <div class="swiper-slide">
            <a href="javascript:" class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/1.jpg" alt="">
              </div>
              <span>甜品饮品</span>
            </a>
            <a href="javascript:" class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/2.jpg" alt="">
              </div>
              <span>商超遍历</span>
            </a>
            <a href="javascript:" class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/3.jpg" alt="">
              </div>
              <span>美食</span>
            </a>
            <a href="javascript:" class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/4.jpg" alt="">
              </div>
              <span>简餐</span>
            </a>
            <a href="javascript:" class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/5.jpg" alt="">
              </div>
              <span>新店特惠</span>
            </a>
            <a href="javascript:" class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/6.jpg" alt="">
              </div>
              <span>准时达</span>
            </a>
            <a href="javascript:" class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/7.jpg" alt="">
              </div>
              <span>预定早餐</span>
            </a>
            <a href="javascript:" class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/8.jpg" alt="">
              </div>
              <span>土豪推荐</span>
            </a>
          </div>
        </div>
        <div class="swiper-pagination"></div>
      </div>
    </nav>
    <!--首页附近商家-->
    <div class="msite_shop_list">
      <div class="shop_header">
        <ShopList></ShopList>
        <i class="iconfont icon-xuanxiang"></i>
        <span class="shop_header_title">附近商家</span>
      </div>
    </div>
  </section>
</template>

<script>
  import HeaderTop from '../../components/HeaderTop/HeaderTop'
  import Swiper from 'swiper'
  import 'swiper/dist/css/swiper.min.css'
  import ShopList from '../../components/ShopList/ShopList'
    export default {
        mounted(){
          //创建一个swiper实例对象，来实现轮播
          new Swiper('.swiper-container',{
            loop:true,
            pagination:{
              el:'.swiper-pagination'
            },
          })
        },
        components:{
          HeaderTop,
          ShopList
        }
    }
</script>

<style lang="stylus" rel="stylesheet/stylus">
  @import "../../common/stylus/mixins.styl"
  .msite
    width 100%
    /*.miste-content-wrapper
      position fixed
      top: 45px
      bottom: 46px
      width: 100%*/
  .msite_nav
    bottom-border-1px(#e4e4e4)
    height 200px
    background #fff
    top 45px
    .swiper-container
      width 100%
      height 100%
      .swiper-wrapper
        width 100%
        height 100%
        .swiper-slide
          display flex
          justify-content center
          align-items flex-start
          flex-wrap wrap
          .link_to_food
            width 25%
            .food_container
              display block
              width 100%
              text-align center
              padding-bottom 10px
              font-size 0
              img
                display inline-block
                width 50px
                height 50px
            span
              display block
              width 100%
              text-align center
              font-size 13px
              color #666
      .swiper-pagination
        >span.swiper-pagination-bullet-active
          background #02a774
  .msite_shop_list
    top-border-1px(#e4e4e4)
    margin-top 10px
    background #fff
    top: 40px;
    .shop_header
      padding 10px 10px 0 10px
      .shop_icon
        margin-left 5px
        color #999
      .shop_header_title
        color #999
        font-size 14px
        line-height 20px
</style>
