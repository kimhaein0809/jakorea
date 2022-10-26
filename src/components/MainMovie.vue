<template>
  <div class="videoSec">
    <div class="wrap">
        <div class="container txtWrap">
            <h5 class="text-center">우리 청소년들이 미래의 인재로 성장하도록</h5>
            <h1>JA KOREA가 함께합니다.</h1>
            <a href="#" class="btn">
                <p class="mb-0 btnt">자세히 보기<i class="fa-solid fa-arrow-right-long"></i></p>
             </a>
        </div>
        <video id="myVideo" autoplay muted loop>
            <source src="../../public/images/02iconBanner/main-home-01-2.mp4">
        </video>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss">
@media (max-width: 991px) {

}
   .videoSec{
    margin-bottom: 180px;
    .wrap{
        width: 100%;
        height: 900px;
        text-align: left;
        display: flex;
        align-items: center;
    }
    .txtWrap{
        z-index: 1;
        color: white;
        h5{
            font-size: 38px;
            width: 750px;
            font-weight: lighter;
            padding: 2px;
            background: linear-gradient(to right, #00a0af, #00a0af);;
        }
        h1{font-size: 75px;font-weight: bold;}
        .btn{
            background: linear-gradient(#00a0af, #00a0af);
            color: white;
            margin-top: 82px;
            padding: 22px 35px;
            border-radius: 40px;
            box-shadow: 0 0 17px 6px rgb(0 0 0 / 9%);
            i{
                margin-left: 48px;
            }
            
        }
        a:hover {
    color: white !important;
}
    }
    #myVideo{
        width: 100%;
        height: 100vh;
        object-fit: cover;
        position: absolute;
        
    }
   }
    
</style>