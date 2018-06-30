<template>
  <div class="wapper">
    <swiper :options="swiperOption">
      <swiper-slide v-for="item of swiperList" :key="item.id" >
        <img class="swipper-img" :src="item.imgUrl">
      </swiper-slide>
      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwipper',
  data: function () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [{
        id: '0001',
        imgUrl: 'https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1530333598733&di=d29f54353b1cf6ff0638b058c5b3d960&imgtype=0&src=http%3A%2F%2Fztd00.photos.bdimg.com%2Fztd%2Fw%3D700%3Bq%3D50%2Fsign%3D7e09ae5cd133c895a67e9a7be12802cd%2F5243fbf2b2119313c153267b6d380cd790238ded.jpg'
      }, {
        id: '0002',
        imgUrl: 'https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1530333637617&di=d878d4dfecea4ec9bca6f66e39d7d9fd&imgtype=0&src=http%3A%2F%2F5b0988e595225.cdn.sohucs.com%2Fimages%2F20180225%2F2fdafc4c8d894ff591774a117040e031.jpeg'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  .wapper >>> .swiper-pagination-bullet-active
    background: #fff
  .wapper
    overflow: hidden
    width: 100%
    height: 0
    padding-bottom: 31.25%
    background: #eee
    .swipper-img
      width: 100%
</style>
