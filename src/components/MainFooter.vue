<template>
  <div class="footer">
      <div class="footTop">
        <div class="container">
            <div class="footinner d-flex align-items-center">
                <ul class="d-flex gap-4">
                    <li><a href="#">이용약관</a></li>
                    <li><a href="#">개인정보처리방침</a></li>
                    <li><a href="#">이메일수집거부</a></li>
                    <li><a href="#">오시는길</a></li>
                </ul>
                <div class="dropup-center dropup">
                    <button class="btn dropdown-toggle" type="button" data-bs-toggle="dropdown" aria-expanded="false">
                        관련 사이트 보기
                    </button>
                    <ul class="dropdown-menu">
                        <li><a class="dropdown-item" href="#">JA Worldwide</a></li>
                        <li><a class="dropdown-item" href="#">JA Afica</a></li>
                        <li><a class="dropdown-item" href="#">JA Americas</a></li>
                        <li><a class="dropdown-item" href="#">JA Asia Pacific</a></li>
                        <li><a class="dropdown-item" href="#">JA Europe</a></li>
                        <li><a class="dropdown-item" href="#">JA Middle East / INJAZ AI-Arab</a></li>
                        <li><a class="dropdown-item" href="#">JA U.S.A</a></li>
                    </ul>
                </div>
            </div>
        </div>
    </div>
    <div class="footBtm pb-4">
        <div class="container">
            <div class="btm1 d-flex py-4">
                <ul class="d-flex gap-4">
                    <li><a href="#">후원하기</a></li>
                    <li><a href="#">온라인 학습관리</a></li>
                    <li><a href="#">기부금영수증</a></li>
                    <li><a href="#">국세청 공시 및 공개 내역</a></li>
                    <li><a href="#">1:1 문의</a></li>
                </ul>
                <div class="sns">
                    <p>Follow SNS</p>
                    <div class="iconWrap">
                        <a href="#"><i class="fa-brands fa-facebook"></i></a>
                        <a href="#"><i class="fa-brands fa-instagram"></i></a>
                        <a href="#"><i class="fa-brands fa-youtube"></i></a>
                    </div>
                </div>
            </div>
            <div class="logo mb-md-5">
                <img src="../assets/images/footer-logo.svg" alt="">
            </div>
            <p>서울특별시 강서구 양천로 583, B동 1408호(염창동, 우림블루나인비즈니스센터) 사단법인 제이에이코리아    우편번호 : 07547    대표 : 이은형    사업자번호 : 107-82-10367</p>
            <p>대표전화 : 02-783-2367    팩스 : 070-4275-5115    이메일 : jakorea@jakorea.org</p>
            <p>ⓒJA Korea,2022</p>
        </div>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss">
dl, ol, ul {
    margin-top: 0;
    margin-bottom: 0 !important
}
    .footer{
        p{color: #aaa;font-size: 15px;}
        img{
            opacity: .5;
        }
        .footTop{
            padding: 20px 0;
            background: #f5f5f5;
            .footinner{
                justify-content: space-between;
                a{
                    color: #777;
                }
            }
            .dropdown-menu{
                border-radius: 10px;
                .dropdown-item{
                    color: #939393;
                }
            }
            .btn{
                background: white;
                border-radius: 20px;
                color: #939393;
                width: 237px;
                padding: 10px 20px;
                display: flex;align-items: center;justify-content: space-between;
            }
        }
        
        .footerBtm{
            background: #fff;
        }
        .btm1{
            justify-content: space-between;
            a{
                color: #767676;
                font-weight: bold;
            }
            .sns{
                color: #aaa;
                font-weight: bold;
                a{
                    color: #aaa;
                    font-size: 20px;
                    margin-right: 30px;
                }
            }
        }
    }
    @media (max-width: 991px) {
        
    .footer{
        a{font-size: 12px;}
        p{color: #aaa;font-size: 12px;}

        img{
            opacity: .5;
            width: 100px;
        }
        .footTop{
            padding: 20px 0;
            background: #f5f5f5;
            .footinner{
                justify-content: space-between;
                a{
                    color: #777;
                }
            }
            .dropdown-menu{
                border-radius: 10px;
                .dropdown-item{
                    color: #939393;
                }
            }
            .btn{
                background: white;
                border-radius: 20px;
                color: #939393;
                width: 150px;
                padding: 10px 20px;
                font-size: 12px;
                display: flex;align-items: center;justify-content: space-between;
            }
        }
        
        .footerBtm{
            background: #fff;
        }
        .btm1{
            justify-content: space-between;
            flex-direction: column;
            gap: 20px;
            a{
                color: #767676;
                font-weight: bold;
            }
            .sns{
                color: #aaa;
                font-weight: bold;
                a{
                    color: #aaa;
                    font-size: 20px;
                    margin-right: 30px;
                }
            }
        }
    }
    }
</style>