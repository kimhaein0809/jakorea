<template>
  <header-view></header-view>
  <main-visual></main-visual>
  <main-banner :banData="bData"></main-banner>
  <main-education></main-education>

</template>

<script>
  import HeaderView from "./components/HeaderView.vue"
  import MainVisual from "./components/MainVisual.vue"
  import MainBanner from "./components/MainBanner.vue"
  import MainEducation from "./components/MainEducation.vue"

  import bData from "@/data/02iconBanner.js";

export default {
  components:{
    HeaderView,
    MainVisual,
    MainBanner,
    MainEducation
},
data(){
  return{
    bData: bData,
  }
}
}
</script>

<style lang="scss">
 @import url(./assets/style.css);


</style>