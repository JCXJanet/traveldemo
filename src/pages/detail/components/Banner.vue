<template>
    <div>
        <div class="banner" @click="handleBannerClick">
            <img class="banner-img" src="//img1.qunarzz.com/sight/p0/1602/68/68aa05adb5315f9990.water.jpg_600x330_0dcecae1.jpg" />
            <div class="banner-info">
                <div class="banner-title">
                    北京海洋馆(AAAA景区)
                </div>
                <div class="banner-number">
                    <span class="iconfont banner-icon">&#xe6dd;</span>
                    30
                </div>
            </div>
        </div>
        <common-gallary
                :imgs="imgs"
                v-show="showGallary"
                @close="handleGalaryClose"
        ></common-gallary>
    </div>
</template>

<script>
import CommonGallary from 'common/gallary/Gallary'
export default {
  name: 'DetailBanner',
  data () {
    return {
      showGallary: false,
      imgs: ['http://img1.qunarzz.com/sight/p0/1602/68/68aa05adb5315f9990.water.jpg_200x200_ce3d2658.jpg', 'http://img1.qunarzz.com/sight/p0/1602/67/67feeab24cfc82bb90.water.jpg_200x200_af2a01b1.jpg']
    }
  },
  methods: {
    handleBannerClick () {
      this.showGallary = true
    },
    handleGalaryClose () {
      this.showGallary = false
    }
  },
  components: {
    CommonGallary
  }
}
</script>

<style lang="stylus" scoped>
    .banner
        position : relative
        overflow : hidden
        height : 0
        padding-bottom :55%
        .banner-img
            width : 100%
        .banner-info
            display : flex
            position : absolute
            left : 0
            right : 0
            bottom : 0
            line-height : .6rem
            color : #fff
            background-image : linear-gradient(top, rgba(0, 0, 0, 0), rgba(0, 0, 0, 0.8))
            .banner-title
                flex : 1
                font-size : .32rem
                padding : 0 .2rem
            .banner-number
                height : .32rem
                line-height : .32rem
                margin-top : .14rem
                padding : 0 .4rem
                border-radius : .2rem
                background : rgba(0, 0, 0, .8)
                font-size : .24rem
                .banner-icon
                    font-size : .24rem
</style>
