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
  <main-notice :noData="nData" :reData="rData"></main-notice>
  <main-movie></main-movie>
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

  import bData from "@/data/02iconBanner.js";
  import eData from "@/data/03eduProgram.js";
  import nData from "@/data/07notice.js"
  import notice from "@/data/04notice.js";
  import story from "@/data/05story.js";
  import news from "@/data/06news.js";
  import rData from "@/data/08result.js"
import MainNotice from './components/MainNotice.vue'

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
    MainMovie
},
data(){
  return{
    bData: bData,
    eData: eData,
    notice: notice,
    story: story,
    news: news,
    nData: nData,
    rData: rData
  }
}
}
</script>

<style lang="scss">
 @import url(./assets/style.css);


</style>