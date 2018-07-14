<template>
    <div class="wrapper">
         <swiper :options="swiperOption" v-if="showSwiper">
        <!-- slides -->
        <swiper-slide v-for="item of list" :key="item.id">
            <img class="swiper-img" :src="item.imgUrl"/>
        </swiper-slide>
        <!-- Optional controls -->
        <div class="swiper-pagination"  slot="pagination"></div>
        <!-- 控制左右箭头 -->
        <!-- <div class="swiper-button-prev" slot="button-prev"></div>
        <div class="swiper-button-next" slot="button-next"></div> -->
        <!-- 灰色滚动条 -->
        <!-- <div class="swiper-scrollbar"   slot="scrollbar"></div> -->
      </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  props: {
    list: Array
  },
  data () {
    return {
      swiperOption: {
        // 控制按钮，轮播图上的小点
        pagination: '.swiper-pagination',
        loop: true
      }
    }
  },
  computed: {
    showSwiper () {
      return this.list.length
    }
  }

}
</script>

<style lang="stylus" scoped>
// ">>>"的意思是穿透，让.wrapper下面所有子组件里只变成白色，不受scope限制
.wrapper >>> .swiper-pagination-bullet-active
    background: #fff
.wrapper
    /* 解决抖动方案*/
    /*width:100%;height:30.47vw会有兼容问题*/
    overflow: hidden
    width: 100%
    height: 0
    padding-bottom: 30.47%
    background: #eee
   .swiper-img
      width: 100%
</style>
