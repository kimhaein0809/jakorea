<template>
  <div class="news">
      <div class="container bg position-relative">
        <form action="">
            <h1>JA Korea 뉴스레터 구독하기</h1>
            <div class="d-flex gap-4">
                <div class="name position-relative">
                    <i class="fa-regular fa-user position-absolute text-white"></i>
                    <input type="text" name="name" placeholder="이름">
                </div>
                <div class="email position-relative">
                    <i class="fa-regular fa-envelope position-absolute text-white"></i>
                    <input type="text" name="email" placeholder="이메일">
                </div>
                <div class="btn">
                    신청하기
                </div>
            </div>
            <div class="check">
                <label for="agree01" class="d-flex align-items-center">
                    <input type="checkbox" class="checkbox position-relative">
                    <i class="fa-regular fa-circle-check off"></i>
                    <i class="fa-solid fa-circle-check on"></i>
                    <p>뉴스레터 구독을 위한 이름 및 이메일 주소 수집에 동의합니다.</p>
                </label>
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
    .check{
        .checkbox{
            opacity: 0;
            z-index: 1;
            margin-left: 5px;
            cursor: pointer;
            height: 20px;
        }
        .off{
            position: absolute;
            font-size: 24px;
            color: #285f74;
            cursor: pointer;
        }
        .on{
            position: absolute;
            font-size: 24px;
            color: white;
            cursor: pointer;
            display: none;
            &.active{
                display: block;
            }
        }
        p{
            margin-top: 1rem;
            padding-left: 20px;
            color: white;
            font-weight: bold;
            font-size: 18px;
        }
    }
    .email,.name{
        i{
            font-size: 24px;
            left: 24px;top: 24px;
            &.active{

            }
        }
    }
    .imgWrap{
        width: 300px;
        bottom: 46px;
        right: 54px;
    }
    .bg{
        padding:46px 54px ;
        border-radius: 20px;
        background: linear-gradient( -45deg,#00a0af,#00c0ca,#00c0ca,#00a0af);
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