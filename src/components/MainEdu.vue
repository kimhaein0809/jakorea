<template>
  <div class="section container">
    <div class="edutop">
        <h1>JA 교육 프로그램</h1>
        <ul v-for="(item,i) in eduData" :key="i">
            <li>
                <button v-html="item.name"></button>
            </li>
        </ul>
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
        ul{
            margin-left: 35px;
            li{
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