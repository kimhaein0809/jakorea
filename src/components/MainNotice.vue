<template>
  <div class="notice">
    <div class="container d-flex">
      <div class="noticeBox">
        <div class="noTop pb-4">
          <h1>모집공고</h1>
        </div>
        <div class="noBtm" v-for="(item,i) in noData" :key="i">
          <div class="noItem">
              <a href="#">
                <span class="tag">모집중</span>
                <div class="bdtxt">
                  <h3>{{item.title}}</h3>
                  <p>{{item.date}}</p>
                </div>
              </a>
            </div>
          </div>
      </div>
      <div class="noticeBox">
        <div class="noTop pb-4">
          <h1>결과발표</h1>
        </div>
        <div class="noBtm" v-for="(item,i) in noData" :key="i">
          <div class="noItem">
              <a href="#">
                <span class="tag">모집중</span>
                <div class="bdtxt">
                  <h3>{{item.title}}</h3>
                  <p>{{item.date}}</p>
                </div>
              </a>
            </div>
          </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
    props:["noData"]
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
  }
  .noItem{
    border-bottom: 1px solid #e7eced;
    position: relative;
  transition: .3s;
  a{
    display: flex;
    align-items: flex-start;
    padding: 35px 25px;
    border-radius: 26px;
    transition: .3s;
    position: relative;
    width: 100%;
  }
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

</style>