<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
      <swiper-slide v-for="item of swiperList" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl" />
      </swiper-slide>
      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        loop: true,
        pagination: {
          el: '.swiper-pagination'
        }
      },
      swiperList: [{
        id: '0001',
        imgUrl: 'http://y.gtimg.cn/music/common/upload/MUSIC_FOCUS/1736974.jpg'
      }, {
        id: '0002',
        imgUrl: 'http://y.gtimg.cn/music/common/upload/MUSIC_FOCUS/1736974.jpg'
      }]
    }
  }
}
</script>
<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination-bullet
    background: rgba(255,255,255,.45) !important
  .wrapper >>> .swiper-pagination-bullet-active
      background: white !important
  .wrapper
    overflow: hidden
    width: 100%
    height: 0
    padding-bottom: 40%
    background: #969696
    .swiper-img
      width: 100%
</style>
