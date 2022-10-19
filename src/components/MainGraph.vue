<template>
  <div class="graph">
    <div class="container">
      <div class="row align-items-center">
        <div class="col-lg-6 imgW">
          <div class="imageF">
            <img src="../../public/images/main-number-1.jpg" alt="">
          </div>
        </div>
        <div class="col-lg-6">
          <ul>
            <li>
              <div class="numT d-flex align-items-center">
                <div class="line"></div>
                <h1>+200</h1>
              </div>
              <div class="numB d-flex align-items-center">
                <h4>지역 네트워크</h4>
                <p>전국 17개 시도 200개이상의 지역에서 교육하고 있습니다.</p>
              </div>
            </li>
            <li>
              <div class="numT d-flex align-items-center">
                <div class="line"></div>
                <h1>+1,000</h1>
              </div>
              <div class="numB d-flex align-items-center">
                <h4>학교 및 기관</h4>
                <p>전국 1,000여개 학교 및 기관, 단체와 협업하여 교육을 진행합니다.</p>
              </div>
            </li>
            <li>
              <div class="numT d-flex align-items-center">
                <div class="line"></div>
                <h1>+3,000</h1>
              </div>
              <div class="numB d-flex align-items-center">
                <h4>교육 진행자</h4>
                <p>3,000여명의 전문 지식을 갖춘 봉사자와 교사, 강사가 함께 교육을 진행하고 있습니다.</p>
              </div>
            </li>
            <li>
              <div class="numT d-flex align-items-center">
                <div class="line"></div>
                <h1>+90,000</h1>
              </div>
              <div class="numB d-flex align-items-center">
                <h4>교육 수혜자</h4>
                <p>전국 90,000여명의 청소년들이 교육 프로그램에 참여합니다.</p>
              </div>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss">
  .graph{
    padding: 100px 0;
    margin-bottom: 180px;
    background: -webkit-gradient(linear, 0% 0%, 100% 0%, from(rgb(2, 157, 173)), to(rgb(0, 142, 159)));
    .imageF{
      width: 400px;
      border-radius: 30px;
      overflow: hidden;
      display: inline-block;
      img{width: 100%;height: 100%;}
    }
  }
 .numT{
  .line{
    height: 10px;
    background: rgba(255,255,255,.5);
    border-radius: 5px;
    position: relative;
    margin-right: 13px;
    width: 75%;
    display: inline-block;
  }
  h1{
      font-size: 30px;
      font-weight: bold;
      color: white;
    }

 }
 .numB{
  h4{
    font-size: 16px;
    font-weight: bold;
    color: white;
    margin-right: 10px;
    margin-bottom: 0;
  }
  p{
    font-size: 14px;
    margin-bottom: 0;
    color: rgba(255,255,255,.5);
  }
 }
@media (max-width: 1399px) {

}
@media (max-width: 1199px) {

}
@media (max-width: 991px) {
.imgW{
  display: flex;align-items: center;justify-content: center;margin-bottom: 20px;
}
}
@media (max-width: 767px) {
  
}
@media (max-width: 575px) {
  
}
</style>