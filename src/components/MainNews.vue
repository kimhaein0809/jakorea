<template>
  <div class="news">
      <div class="container bg position-relative">
        <form action="">
            <h1>JA Korea 뉴스레터 구독하기</h1>
            <div class="d-flex gap-4">
                <input type="text" name="name" placeholder="이름">
                <input type="text" name="email" placeholder="이메일">
                <div class="btn">
                    신청하기
                </div>
            </div>
        </form>
        <div class="imgWrap position-absolute"><img src="../../public/images/subscribe-img.png" alt="" class="w-100"></div>
      </div>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss">
.news{
    margin-bottom: 180px;
    .imgWrap{
        width: 300px;
        bottom: 46px;
        right: 54px;
    }
    .bg{
        padding:46px 54px ;
        border-radius: 20px;
        background: -webkit-gradient(linear, 0% 0%, 100% 0%, from(rgb(2, 157, 173)), to(rgb(0, 142, 159)));;
    }
    form{
        h1{
            font-size: 30px;
            color: white;
            font-weight: bold;
            margin-bottom: 30px;
        }
        input{
            height: 70px;
            border-radius: 10px;
            border: none;
            background: rgba(255,255,255,0.1);
            padding: 0 50px 0 70px;
            font-size: 18px;
            overflow: hidden;
            &::placeholder {
                    font-weight: 400;
                    color: white;
                }
        }
        .btn{
            border-color: white;
            padding: 20px 40px;
            border-radius: 10px;
            color: white;
            &:hover{
                background: white;
                color: rgb(0, 128, 150);
            }
        }
    }
}
    
</style>