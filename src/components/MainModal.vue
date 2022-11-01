<template>
  <div class="modal" :class="{'d-block':mView}">
    <div class="modal-dialog">
        <div class="modal-content">
            <div class="modal-header">
                <h5 class="modal-title">
                    {{banData[mData].title}}
                </h5>
                <button type="button" class="btn-close" @click="$emit('closeModal')"></button>
            </div>
            <div class="modal-body d-flex gap-5">
                <div class="subImg">
                    <img :src="`./images/07notice/${banData[mData].s_src}`" alt="">
                </div>
                <div class="subTxt py-4">
                    <p class="mb-4"><span>대상</span><br>{{banData[mData].target}}</p>
                    <p class="mb-4"><span>모집</span><br>{{banData[mData].recruitment}}</p>
                    <p class="mb-4"><span>발표</span><br>{{banData[mData].announcement}}</p>
                    <p class="mb-4"><span>운영</span><br>{{banData[mData].operate}}</p>
                    <p class="mb-4"><span>후원사</span><br>{{banData[mData].sponsor}}</p>
                </div>
            </div>
        </div>
    </div>
  </div>
</template>

<script>
export default {
    props:[
        "mData","mView","banData"
    ]
}
</script>

<style lang="scss">
    .modal{
        --bs-modal-width: 1000px;
    }
    .subImg{
        width: 500px;
        border-radius: 20px;
        overflow: hidden;
    }
    img{width: 100%;}
    .subTxt{
        p span{font-weight: bold;font-size: 18px;}
    }
</style>