<template>
  <section class="msite">
    <!--首页头部-->
    <header class="header">
          <span class="header_search">
            <i class="iconfont icon-sousuo"></i>
          </span>
      <span class="header_title">
            <span class="header_title_text ellipsis">金隅·观澜时代天筑</span>
          </span>
      <span class="header_login">
            <span class="header_login_text">登录|注册</span>
          </span>
    </header>
    <!--头部组件和插槽-->
    <header-top title="金隅·观澜时代天筑">
         <span class="header_search" slot="left">
            <i class="iconfont icon-sousuo"></i>
         </span>
         <span class="header_login" slot="right">
            <span class="header_login_text">登录|注册</span>
         </span>
    </header-top>
    <!--首页导航-->
    <nav class="msite_nav">
      <div class="swiper-container">
        <div class="swiper-wrapper">
          <div class="swiper-slide">
            <a href="javascript:" class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/meishi.jpeg">
              </div>
              <span>美食</span>
            </a>
            <a href="javascript:" class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/chaoshi.jpeg">
              </div>
              <span>商超便利</span>
            </a>
            <a href="javascript:" class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/shuiguo.jpeg">
              </div>
              <span>水果</span>
            </a>
            <a href="javascript:" class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/yiyao.jpeg">
              </div>
              <span>医药健康</span>
            </a>
            <a href="javascript:" class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/xianhua.jpeg">
              </div>
              <span>浪漫鲜花</span>
            </a>
            <a href="javascript:" class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/paotui.jpeg">
              </div>
              <span>跑腿代购</span>
            </a>
            <a href="javascript:" class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/hanbao.jpeg">
              </div>
              <span>汉堡披萨</span>
            </a>
            <a href="javascript:" class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/shengxian.jpeg">
              </div>
              <span>厨房生鲜</span>
            </a>
            <a href="javascript:" class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/zhaji.jpeg">
              </div>
              <span>炸鸡炸串</span>
            </a>
            <a href="javascript:" class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/difang.jpeg">
              </div>
              <span>地方菜系</span>
            </a>
          </div>
          <div class="swiper-slide">
            <a href="javascript:" class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/malatang.jpeg">
              </div>
              <span>麻辣烫</span>
            </a>
            <a href="javascript:" class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/sushi.jpeg">
              </div>
              <span>速食简餐</span>
            </a>
            <a href="javascript:" class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/difangxiaochi.jpeg">
              </div>
              <span>地方小吃</span>
            </a>
            <a href="javascript:" class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/dapai.jpeg">
              </div>
              <span>大牌惠吃</span>
            </a>
            <a href="javascript:" class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/mifen.jpeg">
              </div>
              <span>米粉面馆</span>
            </a>
            <a href="javascript:" class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/baozi.jpeg">
              </div>
              <span>包子粥店</span>
            </a>
          </div>
        </div>
        <!-- Add Pagination -->
        <div class="swiper-pagination"></div>
      </div>
    </nav>
    <!--首页附近商家-->
    <div class="msite_shop_list">
      <div class="shop_header">
        <i class="iconfont icon-dingdan"></i>
        <span class="shop_header_title">附近商家</span>
      </div>
      <shop-list></shop-list>
    </div>
  </section>
</template>

<script>
  import HeaderTop from '../../components/HeaderTop/HeaderTop'
  import ShopList from '../../components/ShopList/ShopList'
  import Swiper from 'swiper'
  import 'swiper/dist/css/swiper.min.css'
export default {
  name: 'Order',
  components: {HeaderTop, ShopList},
  // 创建一个swiper实例对象
  mounted () {
    /* eslint-disable no-new */
    new Swiper('.swiper-container', {
      loop: true, // 循环播放
      // 如果需要分页器
      pagination: {
        el: '.swiper-pagination'
      }
    })
  }
}
</script>

<style scoped lang="stylus" rel="stylesheet/stylus">
  @import "../../common/stylus/mixins.styl"
  &.msite  //首页
    width 100%
    .msite_nav
      bottom-border-1px(#e4e4e4)
      margin-top 45px
      height 200px
      background #fff
      .swiper-container
        width 100%
        height 100%
        .swiper-wrapper
          width 100%
          height 100%
          .swiper-slide
            display flex
            //取消居中
            /*justify-content center*/
            align-items flex-start
            flex-wrap wrap
            .link_to_food
              width 20%
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
      .shop_header
        padding 10px 10px 0
        .shop_icon
          margin-left 5px
          color #999
        .shop_header_title
          color #999
          font-size 14px
          line-height 20px

</style>
