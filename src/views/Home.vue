<template>
  <div>
    <div class="swiper-container">
      <div class="swiper-wrapper">
        <div class="swiper-slide slide1">Slide 1</div>
        <div class="swiper-slide slide2">Slide 2</div>
        <div class="swiper-slide slide3">Slide 3</div>
      </div>
      <!-- 如果需要分页器 -->
      <div class="swiper-pagination"></div>
     
    </div>
  </div>
</template>

<script>
import Swiper from 'swiper'
import 'swiper/css/swiper.css'
export default {
  data() {
    return {
      msg: 'Home 组件'
    }
  },
  mounted () {
    new Swiper ('.swiper-container', {
      // direction: 'vertical', // 垂直切换选项
      loop: true, // 循环模式选项
      // autoplay: true,
      autoplay: {
        duration: 3000
      },
     
      // 如果需要分页器
      pagination: {
        el: '.swiper-pagination',
      }
     
    }) 
  }
}
</script>

<style lang="scss" scoped>
  .swiper-container{
    height:200px;
    .swiper-slide{
      height:100%;
      line-height: 200px;
      font-size: 20px;
      color: #ffffff;
    }
    .slide1{
      background: red;
    }
    .slide2{
      background: yellowgreen;
    }
    .slide3{
      background: blueviolet;
    }
  }
</style>