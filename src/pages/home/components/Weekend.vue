<template>
<div>
  <div class="title">周末去哪儿</div>
  <ul>
    <li class="item border-bottom" v-for="item of weekendList" :key="item.id">
        <div class="item-img-wrapper">
          <img class="item-img" :src="item.imgUrl" alt="">
        </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
        </div>
    </li>
  </ul>
</div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  data () {
    return {
      weekendList: [{
        id: '0001',
        imgUrl: 'https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1530413369112&di=31264b0e3183fbbfbfc51559a709ea5b&imgtype=0&src=http%3A%2F%2Fqiniuimg.qingmang.mobi%2Fimage%2Forion%2F4d959ec41ea9b42839d28757fd7f7a76_640_214.jpeg',
        title: '海上世界',
        desc: '这里是一个好玩的不得了的海上世界'
      }, {
        id: '0002',
        imgUrl: 'https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1530413369112&di=31264b0e3183fbbfbfc51559a709ea5b&imgtype=0&src=http%3A%2F%2Fqiniuimg.qingmang.mobi%2Fimage%2Forion%2F4d959ec41ea9b42839d28757fd7f7a76_640_214.jpeg',
        title: '海上世界',
        desc: '这里是一个好玩的不得了的海上世界'
      }, {
        id: '0003',
        imgUrl: 'https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1530413369112&di=31264b0e3183fbbfbfc51559a709ea5b&imgtype=0&src=http%3A%2F%2Fqiniuimg.qingmang.mobi%2Fimage%2Forion%2F4d959ec41ea9b42839d28757fd7f7a76_640_214.jpeg',
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
    line-height: .8rem
    background: #ccc
    text-indent: .2rem
  .item-img-wrapper
    overflow: hidden
    height: 0
    padding-bottom: 33.9%
    .item-img
      width: 100%
  .item-info
    padding: .1rem
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
</style>
