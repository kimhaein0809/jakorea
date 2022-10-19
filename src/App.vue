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
</template>

<script>
  import HeaderView from "./components/HeaderView.vue"
  import MainVisual from "./components/MainVisual.vue"
  import MainBanner from "./components/MainBanner.vue"
  import MainEdu from "./components/MainEdu.vue"
  import MainEducation from "./components/MainEducation.vue"
  import MainGraph from "./components/MainGraph.vue"

  import VisualTap from "./components/VisualTap.vue"

  import bData from "@/data/02iconBanner.js";
  import eData from "@/data/03eduProgram.js";

  import notice from "@/data/04notice.js";
  import story from "@/data/05story.js";
  import news from "@/data/06news.js"

export default {
  components:{
    HeaderView,
    MainVisual,
    MainBanner,
    MainEdu,
    MainEducation,
    MainGraph,
    VisualTap,
},
data(){
  return{
    bData: bData,
    eData: eData,
    notice: notice,
    story: story,
    news: news,
  }
}
}
</script>

<style lang="scss">
 @import url(./assets/style.css);


</style>