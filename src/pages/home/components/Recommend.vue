<template>
<div>
  <div class="title">热销推荐</div>
  <ul>
    <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <img class="item-img" :src="item.imgUrl" alt="">
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-button">查看详情</button>
        </div>
    </li>
  </ul>
</div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1530410845845&di=3035c7386a9621c22842079b723ce1fd&imgtype=0&src=http%3A%2F%2Fwww.g-photography.net%2Ffile_news%2Fcover%2F13870.jpg',
        title: '海上世界',
        desc: '这里是一个好玩的不得了的海上世界'
      }, {
        id: '0002',
        imgUrl: 'https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1530410845845&di=3035c7386a9621c22842079b723ce1fd&imgtype=0&src=http%3A%2F%2Fwww.g-photography.net%2Ffile_news%2Fcover%2F13870.jpg',
        title: '海上世界',
        desc: '这里是一个好玩的不得了的海上世界'
      }, {
        id: '0003',
        imgUrl: 'https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1530410845845&di=3035c7386a9621c22842079b723ce1fd&imgtype=0&src=http%3A%2F%2Fwww.g-photography.net%2Ffile_news%2Fcover%2F13870.jpg',
        title: '海上世界',
        desc: '这里是一个好玩的不得了的海上世界'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .title
    margin-top: .2rem
    line-height: .8rem
    background: #ccc
    text-indent: .2rem
  .item
    overflow: hidden
    display: flex
    height: 1.9rem
    .item-img
      width: 1.7rem
      height: 1.7rem
      padding: .1rem
    .item-info
      flex: 1
      padding: .1rem
      min-width: 0
      .item-title
        line-height: .54rem
        font-size: .32rem
        text-align: left
        ellipsis()
      .item-desc
        line-height: .4rem
        color: #eee
        text-align: left
        ellipsis()
      .item-button
        float: left
        line-height: .44rem
        margin-top: .16rem
        background: #ff9300
        padding: 0 .2rem
        border-radius: .06rem
        color: #fff
</style>
