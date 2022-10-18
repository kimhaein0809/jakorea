<template>
  <div class="section">
      <div class="container">
        <div class="row justify-content-center">
            <div class="col-5 col-md-4 col-lg item" v-for="(item,i) in banData" :key="i">
                <a :href="item.href">
                    <div class="imgWrap"><img :src="`./images/02iconBanner/${item.src}`" alt="" class="w-100"></div>
                    <div class="txt text-center">
                        <p v-html="item.title" class="title"></p>
                        <p v-html="item.subtitle" class="subtitle"></p>
                    </div>
                </a>
            </div>
        </div>
      </div>
  </div>
</template>

<script>
export default {
    props:["banData"]
}
</script>

<style lang="scss">
.section{
    margin-top: 100px;
}
.item{
    :hover{
        img{
            transform: translateY(-20px);
            transition: .5s;
        }
    }
}
.imgWrap{
    height: 170px;
}
    img{
        height: 140px;
    }
.txt{
    .title{
        font-weight: bold;
        font-size: 18px;
    }
    .subtitle{
        font-size: 15px;
    }
}
</style>