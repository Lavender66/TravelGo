<template>
  <div>
    <div class="recommend-title">热销推荐</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <img  class="item-img" :src="item.imgUrl">
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
      recommendList: [ {
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1509/ca/2c5c95c035a9f99ad613fad782798aea.water.jpg_150x150_fc63fdb2.jpg',
        title: '梁子湖龙湾度假村',
        desc: '梁子湖龙湾度假村旅游圣地'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1710/90/909e5d4a6ac636ada3.img.jpg_150x150_13488beb.jpg',
        title: '梵高星空艺术馆',
        desc: '梵高星空艺术馆旅游圣地'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/201403/11/1f70100804193c28f8b71378c0faa49e.jpg_150x150_db8e043b.jpg',
        title: '户部巷',
        desc: '武汉户部巷美食圣地'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .recommend-title
    margin-top: .2rem
    line-height: .8rem
    background: #eee
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
       ellipsis()
     .item-desc
       line-height: .4rem
       color: #ccc
       ellipsis()
     .item-button
       line-height: .44rem
       margin-top: .16rem
       background: #ff9300
       padding: 0 .2rem
       border-radius: .06rem
       color: #fff
</style>
