<template>
  <div class="edu">
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
          v-for="(item) in swiperView"
          :key="item"
          :style="{'background-color':`white`}"
        >
            <!-- <div :style="{'background-color':`${item.color}`}" class="innerItem"> -->
            <div class="container d-flex align-items-center justify-content-center">
                
                <div class="row">
                    <div class="txtW col-7">
                        <h1 v-html="item.title"></h1>
                        <p v-html="item.subtitle" class="mt-3 subt"></p>
                        <a href="#" class="btn">
                            <p class="mb-0 btnt">자세히 보기<i class="fa-solid fa-arrow-right-long"></i></p>
                        </a>
                    </div>
                    <div class="col-5">
                        <div class="imgWrap"><img :src="`./images/03eduProgram/${item.src}`" alt=""></div>
                    </div>
                </div>
            </div>   
            <div class="gray"></div>   
          </swiper-slide>
      
      </swiper>
      <div class="container position-relative">
          <div class="btnWrap ps-3">
            <div class="prev">
              <i class="fa-solid fa-arrow-left-long"></i>
            </div>
            <div class="next">
              <i class="fa-solid fa-arrow-right-long"></i>
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
  
  
  // import required modules
  import { EffectFade, Navigation} from "swiper";
  
  //swiper data
  import sData from "@/data/03eduProgram.js"
  
  export default {
    components: {
      Swiper,
      SwiperSlide,
    },
    setup() {
      return {
        modules: [EffectFade, Navigation],
        swiperView:sData,
        swiperOptions:{
          loop:true,
          navigation:{
            nextEl:'.edu .next',
            prevEl:'.edu .prev',
          },
        }
      };
    },
  };
</script>

<style lang="scss">
.gray{
  position: absolute;
  right: 0;
  bottom: 0;
  top: 0;left: calc(50% + 450px);
  border-top-left-radius: 50px;
  background: #f3f6f7;
}
    .edu{
    margin-left: auto;
    margin-right: auto;
    position: relative;
    overflow: hidden;
    padding: 0;z-index: 1;
    height: 745px;
    .btnWrap{
        gap:1300px;
        display: flex;
        position: absolute;
        bottom: 400px;
        left: 0;
        z-index: 10;
        left: 0;
        .next,.prev{
          color: #A4ADB0;
          font-size: 40px;
          cursor: pointer;
        }
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
        .row{padding-top: 140px;}
      }
    }
  }
  
    .edu{
      position: relative;
      .txtW{
        z-index: 1;
        h1{
            font-weight: bold;
            font-size: 35px;
        }
        p{
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
      .imgWrap{
        img{
          height: 362px;
        }
      }
     
    }
</style>