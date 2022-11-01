<template>
  <header-view></header-view>
  <main-visual></main-visual>
  <main-banner :banData="bData"></main-banner>
  <main-edu :eduData="eData"></main-edu>
  <main-education></main-education>
  <main-graph></main-graph>
  <visual-tap 
    :notice="notice"
    :story="story"
    :news="news"
    >
  </visual-tap>
  <main-notice :noData="nData" :reData="rData" @modalOpen="modalView"></main-notice>
  
  <main-movie></main-movie>
  <main-sponsor :koData="kData"></main-sponsor>
  <main-news></main-news>
  <main-footer></main-footer>
  <div class="start" :class="{end:mView}">
    <main-modal :mView="mView" :mData="mData" :banData="nData" @closeModal="mView=false"></main-modal>
  </div>
</template>

<script>
  import HeaderView from "./components/HeaderView.vue"
  import MainVisual from "./components/MainVisual.vue"
  import MainBanner from "./components/MainBanner.vue"
  import MainEdu from "./components/MainEdu.vue"
  import MainEducation from "./components/MainEducation.vue"
  import MainGraph from "./components/MainGraph.vue"
  import VisualTap from "./components/VisualTap.vue"
  import MainMovie from "./components/MainMovie.vue"
  import MainNews from "./components/MainNews.vue"
  import MainFooter from "./components/MainFooter.vue"
  import MainModal from "./components/MainModal.vue"

  import kData from "@/data/09support.js";
  import bData from "@/data/02iconBanner.js";
  import eData from "@/data/03eduProgram.js";
  import nData from "@/data/07notice.js"
  import notice from "@/data/04notice.js";
  import story from "@/data/05story.js";
  import news from "@/data/06news.js";
  import rData from "@/data/08result.js"
import MainNotice from './components/MainNotice.vue'
import MainSponsor from './components/MainSponsor.vue'

export default {
  components:{
    HeaderView,
    MainVisual,
    MainBanner,
    MainEdu,
    MainEducation,
    MainGraph,
    VisualTap,
    MainNotice,
    MainMovie,
    MainSponsor,
    MainNews,
    MainFooter,
    MainModal
},
data(){
  return{
    bData: bData,
    eData: eData,
    notice: notice,
    story: story,
    news: news,
    nData: nData,
    rData: rData,
    kData: kData,
    mView:false,
    mData:1,
  }
},
methods:{
  modalView(num,name){
    console.log(num,name);
    this.mView = true;
    this.mData = num;
  }
}
}
</script>

<style lang="scss">
 @import url(./assets/style.css);
.start{
  opacity: 0;
  transition: .3s;
  &.end{
    opacity: 1;
  }
}

</style>