<template>
  <div class="tabVisual">
      <div class="container">
        <div class="tabTop d-flex">
            <h2>JA 기관소식</h2>
            <div class="mb-3 d-flex">
                <div class="tab" @click="tab=1" :class="{active:tab==1}">공지사항</div>
                <div class="tab" @click="tab=2" :class="{active:tab==2}">스토리</div>
                <div class="tab" @click="tab=3" :class="{active:tab==3}">언론보도</div>
            </div>
        </div>

        <visual-tap-swiper :notice="notice" :story="story" :news="news" :tab="tab"></visual-tap-swiper>
      </div>
  </div>
</template>

<script>
import VisualTapSwiper from "@/components/VisualTapSwiper.vue"

export default {
    components:{
        VisualTapSwiper,
    },
    props:[
        "notice",
        "story",
        "news"
    ],
    data(){
        return {
            tab:1,
        }
    }
}
</script>

<style lang="scss">
.tabTop{
    align-items: center;
    margin-bottom: 80px;
    h2{
        font-size: 42px;
        margin-right: 40px;
        font-weight: bold;
    }
}
    .tabVisual{
        height: 500px;
        margin-bottom: 100px;
        .tab{
            margin: 0 30px;
            font-size: 20px;
            text-align: center;
            height: 40px;
            position: relative;
            cursor:pointer;
            &.active{
                font-weight: bold;
            }
            &.active:after{
                content:"";
                position: absolute;
                width: 100%;
                height: 4px;
                background: rgb(34, 111, 141);
                left: 0;bottom: 0;
            }
        }


    }
    @media (max-width: 1399px) {

}
@media (max-width: 1199px) {
  

  
}
@media (max-width: 991px) {
    .tabVisual{
        height: 600px;
        margin-bottom: 100px;
        
    }
    .tabTop{
        flex-direction: column;
        align-items: start;
    h2{
        font-size: 40px;
        margin-right: 0px;
        margin-bottom: 20px;
        font-weight: bold;
    }
}
}
@media (max-width: 767px) {
  
}
@media (max-width: 575px) {
  
}
</style>