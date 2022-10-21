<template>
  <div class="section container">
    <div class="edutop">
        <h1>JA 교육 프로그램</h1>
        <div v-for="(item,i) in eduData" :key="i">
            <div class="btn">
                <button v-html="item.name"></button>
            </div>
        </div>
    </div>
  </div>
</template>

<script>
export default {
    props:["eduData"]
}
</script>

<style lang="scss">

    .edutop{
        margin-top: 180px;
        display: flex;align-items: center;
        h1{font-weight: bold;}
        div{
            margin-left: 15px;
            .btn{
            button{
                font-size: 20px;
                border: none;
                background: transparent;
                cursor: pointer;
            }
        }
        }
    }
</style>