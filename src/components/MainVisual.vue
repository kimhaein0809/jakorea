<template>
    <div class="visual">
      <swiper
      :navigation="true"
      :effect="'fade'"
      :modules="modules"
      v-bind="swiperOptions"
      :loop="true"
      :pagination="{
          clickable: true,
        }"
      class="mySwiper"
      >
        <swiper-slide
          v-for="(item,i) in swiperView"
          :key="item"
          :style="{'background-color':`${swiperView[i].color}`}"
        >
            <!-- <div :style="{'background-color':`${item.color}`}" class="innerItem"> -->
            <div class="container d-flex align-items-center h-100">
                <div class="txtW">
                    <h1 v-html="item.mainTitle"></h1>
                    <p v-html="item.subtitle" class="mt-3 subt"></p>
                    <a href="#" class="btn">
                        <p class="mb-0 btnt">자세히 보기<i class="fa-solid fa-arrow-right-long"></i></p> 
                    </a>
                </div>
            </div>    
            <div class="videoWrap">
                <video id="myVideo" autoplay muted loop>
                    <source :src="`./images/01mainSlide_video/${item.src}`">
                </video>
            </div>

        </swiper-slide>
      
      </swiper>
      <div class="container position-relative">
          <div class="btnWrap ps-3">
            <div class="prev">
                <i class="fa-solid fa-chevron-left"></i>
            </div>
            <div class="next">
                <i class="fa-solid fa-chevron-right"></i>
            </div>
          </div>
      </div>
    </div>
  </template>
  <script>
  // Import Swiper Vue.js components
  import { Swiper, SwiperSlide } from "swiper/vue";
  
  // Import Swiper styles
  import "swiper/css";

  import "swiper/css/effect-fade";
  import "swiper/css/navigation";
  import "swiper/css/pagination";
  
  
  // import required modules
  import { EffectFade, Navigation,Pagination } from "swiper";
  
  //swiper data
  import sData from "@/data/01mainSlide.js"
  
  export default {
    components: {
      Swiper,
      SwiperSlide,
    },
    setup() {
      return {
        modules: [EffectFade, Navigation,Pagination],
        swiperView:sData,
        swiperOptions:{
          loop:true,
          navigation:{
            nextEl:'.visual .next',
            prevEl:'.visual .prev',
          },
          pagination:{
            type:'fraction'
          }
        }
      };
    },
  };
  </script>
  <style lang="scss">
  
  .visual{
    margin-left: auto;
    margin-right: auto;
    position: relative;
    overflow: hidden;
    padding: 0;z-index: 1;
    height: 745px;
  }
    .mySwiper{
        position: relative;
        width: 100%;
        height: 100%;
        z-index: 1;
        display: flex;
        transition-property: transform;
        box-sizing: content-box;
      .swiper-slide{
        height: auto;width: 100%;
        .videoWrap{
            width: 1150px;
            left: 45%;
            position: absolute;
            bottom: 0;height: 100%;
            top: 0;
        }
        #myVideo{
            width: 100%;height: 100%;
            padding-top: 40px;
        }
        .innerItem{ 
          height: 100%;
        }
      }
    }
    .visual{
      position: relative;
      .txtW{
        width: 60%;
        z-index: 1;
        color: #285F74;
        h1{
            
            font-size: 66px;
            font-weight: lighter;
            letter-spacing: -5px;
            span{
                font-weight: bold;
            }
        }
        p{
            font-weight: bold;
            &.subt{
                font-size: 18px;
            }
            &.btnt{
                font-size: 17px;
            }

        }
        .btn{
            background: white;
            margin-top: 82px;
            padding: 22px 35px;
            border-radius: 40px;
            box-shadow: 0 0 17px 6px rgb(0 0 0 / 9%);
            i{
                margin-left: 48px;
            }
        }
      }
      .swiper-pagination{
        bottom: 95px;
        left: -606px;
        z-index: 3;
      }
      .btnWrap{
        gap:50px;
        display: flex;
        position: absolute;
        bottom: 90px;
        z-index: 10;
        left: 0;
        .next,.prev{
          color: #A4ADB0;
          font-size: 20px;
          cursor: pointer;
        }
      }
    }
    @media (max-width: 1399px) {

    }
    @media (max-width: 1199px) {
      .visual{
      position: relative;
      .txtW{
        h1{
            
            font-size: 40px;
            font-weight: lighter;
            letter-spacing: -5px;
            span{
                font-weight: bold;
            }
        }
        p{
            font-weight: bold;
            &.subt{
                font-size: 16px;
            }
            &.btnt{
                font-size: 15px;
            }

        }
        .btn{
            background: white;
            margin-top: 20px;
            padding: 14px 18px;
            border-radius: 40px;
            box-shadow: 0 0 17px 6px rgb(0 0 0 / 9%);
            i{
                margin-left: 20px;
            }
        }
      }
    }
    .mySwiper{
      .swiper-slide{
        .videoWrap{
            left: 25%;
        }
      }
    }    
  }
    @media (max-width: 991px) {
      
    }
    @media (max-width: 767px) {
      
    }
    @media (max-width: 575px) {
      
    }
  </style>