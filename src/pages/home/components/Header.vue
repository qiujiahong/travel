<template>
  <div class="header">
      <div class="header-left">
        <div class="iconfont back-icon">&#xe624;</div>
      </div>
      <div class="header-input">
         <span class="iconfont">&#xe632;</span>
        输入城市/景点/游完主题
      </div>
      <router-link to='city'>
        <div class="header-right">
          {{this.city}}
          <span class="iconfont arrow-icon">&#xe64a;</span>
        </div>
      </router-link>
  </div>
</template>

<script>
export default {
  name: 'Header',
  props: {
    city: String
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  .header
    display: flex
    line-height $headerHeight
    background: $bgColor
    color: #fff
    .header-left
      width: .64rem
      float: left
      .back-icon
        text-align: center
        font-size: .4rem
    .header-input
      flex: 1
      height: 0.64rem
      line-height: 0.64rem
      margin-top: .12rem
      margin-left: .2rem
      padding-left: .2rem
      background: #fff
      border-radius: .1rem
      color: #ccc
      text-align: left
    .header-right
      color: #fff
      width: 1.24rem
      float: right
      text-align: center
      .arrow-icon
        margin-left: -.04remp
        font-size: .24rem
</style>
