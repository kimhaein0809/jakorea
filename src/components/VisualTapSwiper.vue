<template>
    <swiper
       v-bind="swiperOptions1"
      :modules="modules1"
      class="mySwiper1"
    >
      <swiper-slide v-if="tab==1" v-for="item in notice" :key="item" :class="{notice:tab=1}">
        <h4>{{item.name}}</h4> 
        <h3>{{item.title}}</h3>
        <br>
        <p class="con">{{item.content}}</p>
      </swiper-slide>

      <swiper-slide v-if="tab==2" v-for="item in story" :key="item" :class="{story:tab=2}">
        <h4>{{item.name}}</h4> 
        <h3>{{item.title}}</h3> 
        <br>
        <p class="con">{{item.subtitle}}</p>

      </swiper-slide>

      <swiper-slide v-if="tab==3" v-for="item in news" :key="item" :class="{news:tab=3}">
        <h4>{{item.name}}</h4>
        <h3>{{item.title}}</h3>
        <br>
        <p class="con">{{item.subtitle}}</p>
      </swiper-slide>

    </swiper>

  </template>
  <script>
  // Import Swiper Vue.js components
  import { Swiper, SwiperSlide } from "swiper/vue";
  
  // Import Swiper styles
  import "swiper/css";
  
  import "swiper/css/pagination";
  import "swiper/css/navigation";
  
 
  
  // import required modules
  import { Pagination, Navigation } from "swiper";
  
  export default {
    components: {
      Swiper,
      SwiperSlide,
    },
    props:[
        "notice",
        "story",
        "news",
        "tab",
    ],
    setup() {
      return {
        modules1: [Pagination, Navigation],
        swiperOptions1:{
            slidesPerView:3,
            spaceBetween:30,
            loop:true,
            observer: true,
            observeParents: true,
        
      }
      }
    },
  };
  </script>
<style lang="scss">
.mySwiper1{
  margin: 0 100px;
}
    .swiper-slide{
      cursor: pointer;
      margin-bottom: 150px;
      h3{
        font-size: 24px;
        font-weight: bold;
      }
      h4{
        display: inline-block;
        background: #000;
        font-size: 13px;
        color: white;
        border-radius: 20px;
        padding: 9px 10px;
        margin-bottom: 18px;
      }
      .con{
        font-size: 18px;
        line-height: 31px;
        display: -webkit-box;
        text-overflow: ellipsis;
        box-orient: vertical;
        word-wrap: break-word;
        height: 100px;
        line-clamp: 3;
        overflow: hidden;
      }
        height: 400px;
    }
</style>
  