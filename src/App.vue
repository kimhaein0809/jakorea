<template>
  <header-view></header-view>
</template>

<script>
import HeaderView from "./components/HeaderView.vue"
export default {
  components:{
    HeaderView,
  }
}
</script>

<style>
  *{margin: 0;padding: 0;}
    ul,li{list-style: none;}
    a:link,a:visited{text-decoration: none;color: #333;}
    .container{
      width: 1280px;
      margin: 0 auto;
    }
</style>