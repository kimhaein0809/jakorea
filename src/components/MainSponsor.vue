<template>
  <div class="spon">
    <div class="container">
      <div class="row">
        <div class="col-md-4 txtW">
          <p>국내외 여러기업이 동참하고 있습니다.</p>
          <h1>JA Korea 후원</h1>
          <a href="#" class="btn">
              <p class="mb-0 btnt">자세히 보기<i class="fa-solid fa-arrow-right-long"></i></p>
          </a>
        </div>
        <swiper
          :effect="'fade'"
          :navigation="true"
          :loop="true"
          :modules="modules"
          class="mySwiper3 col-md-8"
        >
          <swiper-slide>
              <div class="row">
                <div class="col-4" v-for="(item,i) in koData" :key="i">
                  <div class="imgWrap d-flex align-items-center justify-content-center py-5">
                    <img :src="`./images/09support/${item.src}`" alt="">
                  </div>
                </div>
              </div>
          </swiper-slide>
        </swiper>
          <div class="btnWrap1">
            <div class="prev">
              <i class="fa-solid fa-arrow-left-long"></i>
            </div>
            <div class="next">
              <i class="fa-solid fa-arrow-right-long"></i>
            </div>
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
import { EffectFade, Navigation,} from "swiper";

export default {
  props:["koData"],
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    return {
      modules: [EffectFade, Navigation,],
      swiperOptions:{
        loop:true,
        navigation:{
          nextEl:'.spon .next',
          prevEl:'.spon .prev'
        }
      }
    };
  },
}
</script>

<style lang="scss">
.spon{
  margin-bottom: 180px;
  .swiper-button-next, .swiper-button-prev {opacity: 0;}
  .item:hover img{transform: translate(0);}
  img{width: 100px;};
  .imgWrap{
  background: #eee;
  border-radius: 10px;
  height: 80px;
  margin-bottom: 20px;
}
}
ol, ul{margin-left: 0;}

.btnWrap1{
        gap: 30px;
        display: flex;
        z-index: 10;
        .next,.prev{
          color: #A4ADB0;
          font-size: 30px;
          cursor: pointer;
        }
      }

  .txtW{
    p{
      font-weight: bold;
      color: #285f74;
      font-size: 17px;
    }
    h1{
      font-size: 45px;
      font-weight: bold;
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
  @media (max-width: 991px) {
    .spon{
      .btnWrap1{
        display: none;
      }
    }
    .txtW{
      margin-bottom:50px;
      .btn{
        margin-top: 30px;
      }
    }
  }
  
</style>