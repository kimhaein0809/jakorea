<template>
  <div class="notice">
    <div class="container d-flex">
      <div class="noticeBox noBox1">
        <div class="noTop pb-4 ">
          <h1>모집공고</h1>
        </div>
        <div class="noBtm" v-for="(item,i) in noData" :key="i">
          <div class="noItem"  @click="$emit('modalOpen',i,item.name)">
                <span class="tag col-2 text-center">모집중</span>
                <div class="bdtxt">
                  <h3>{{item.title}}</h3>
                  <p>{{item.date}}</p>
                </div>
            </div>
          </div>
      </div>
      <div class="noticeBox">
        <div class="noTop pb-4">
          <h1>결과발표</h1>
        </div>
        <div class="noBtm" v-for="(item,i) in reData" :key="i">
          <div class="noItem" @click="$emit('modalOpen',i,item.name)">
                <div class="bdtxt">
                  <h3>{{item.title}}</h3>
                  <p>{{item.date}}</p>
                </div>
            </div>
          </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
    props:["noData","reData"]
}
</script>

<style lang="scss">
.notice{margin-bottom: 180px;}
.container{justify-content: space-between;}
.noticeBox{width: calc( 50% - 50px );}
.noTop{
  h1{font-size: 35px;font-weight: bold;}
  border-bottom: 2px solid #000;
}
.noBtm{
  .tag{
    padding: 8px 10px;
    background: #285f74;
    margin-right:15px;
    color: white;font-weight: bold;border-radius: 20px;
  }
  .noItem{
    border-bottom: 1px solid #e7eced;
    position: relative;
    transition: .3s;
    cursor: pointer;
    display: flex;
    align-items: flex-start;
    padding: 35px 25px;
    border-radius: 26px;
    transition: .3s;
    position: relative;
    width: 100%;

}
  h3{
    font-size: 22px;font-weight: bold;
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;display: block;
  }
  p{font-size: 16px;color: #7F7F7F;margin-bottom: 0;}
}
.bdtxt{min-width: 0;}

.noItem:hover{
  box-shadow: 0 0 17px 6px rgb(0 0 0 / 9%);
  border-radius: 20px;
}
@media (max-width: 1399px) {

}
@media (max-width: 1199px) {

}
@media (max-width: 991px) {
  .notice{
    .container{
      flex-direction: column;
    }
  }
 
 .noticeBox {
    width: 100%;
}
.noBox1{
  margin-bottom: 40px;
}
}
@media (max-width: 767px) {
  
}
@media (max-width: 575px) {
  
}
</style>