<template>
  <header-view></header-view>
  <main-visual></main-visual>
  <main-banner :banData="bData"></main-banner>
  <main-edu :eduData="eData"></main-edu>
  <main-education></main-education>

</template>

<script>
  import HeaderView from "./components/HeaderView.vue"
  import MainVisual from "./components/MainVisual.vue"
  import MainBanner from "./components/MainBanner.vue"
  import MainEdu from "./components/MainEdu.vue"
  import MainEducation from "./components/MainEducation.vue"

  import bData from "@/data/02iconBanner.js";
  import eData from "@/data/03eduProgram.js";

export default {
  components:{
    HeaderView,
    MainVisual,
    MainBanner,
    MainEdu,
    MainEducation
},
data(){
  return{
    bData: bData,
    eData: eData,
  }
}
}
</script>

<style lang="scss">
 @import url(./assets/style.css);


</style>