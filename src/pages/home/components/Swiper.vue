<template>
  <div class="wrapper">
    <swiper :options="swiperOption" >
    <!-- slides -->
    <swiper-slide v-for="item of swiperList" :key="item.id">
      <img class="swiper-img" :src="item.imgUrl" />
    </swiper-slide>
    
    
    <div class="swiper-pagination"  slot="pagination"></div>
    
   
  </swiper>
  </div>
</template>

<script>
export default {
  name:'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination' , // 左右滑动小点点
        loop:true
      },
      swiperList: [{
        id:'0001',
        imgUrl:'https://imgs.qunarzz.com/vs_ceph_vcimg/c0a60fa20379efa4f02ce527a680dc1b.jpeg'
      }, {
        id:'0002',
        imgUrl:'https://imgs.qunarzz.com/vs_ceph_vcimg/79faa5a73731e84a7731db49d5baa91e.jpeg'
      }]
    }
  }
}

</script>

<style lang="stylus" scoped>
   .wrapper >>> .swiper-pagination-bullet-active
      background: #fff
  .wrapper
    overflow: hidden
    width: 100%
    height: 0
    padding-bottom: 31.25%
    background: #eee
    
  .swiper-img
      width: 100%
</style>