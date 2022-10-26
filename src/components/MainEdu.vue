<template>
  <div class="section container">
    <div class="edutop">
        <h1>JA 교육 프로그램</h1>
        <div class="edubtn">
            <div v-for="(item,i) in eduData" :key="i">
                <div class="pro">
                    <button v-html="item.name"></button>
                </div>
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
    .edubtn{
        display: flex;
        gap: 20px;
    }
    
    .edutop{
        margin-top: 180px;
        display: flex;align-items: center;
        h1{font-weight: bold;margin-right: 20px;}
        div{
            .pro{
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