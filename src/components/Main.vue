<script setup>
import { ref } from 'vue';
let page=ref("introduce"); //用PAGE紀錄響應式狀態,用來決定home/product,預設是home
let change=function(clickpage){
    page.value=clickpage;
}
</script>

<template>
<main>
    <div class="introduce">
        <div class="left">
            <button :class="page==='introduce'?'current':''"  @click="change('introduce')">平台介紹</button>
            <button :class="page==='combination'?'current':''"  @click="change('combination')">智能投資組合</button>
            <button :class="page==='invest'?'current':''"  @click="change('invest')">模擬投資試算</button>
            <button :class="page==='article'?'current':''"  @click="change('article')">知識專欄</button>
            <button :class="page==='personal'?'current':''"  @click="change('personal')">個人化服務</button>
        </div>
        <div class="right">
            <div v-if="page==='introduce'">
                「Coinstep 投資新手村」旨在透過簡單直觀的方式，幫助新手投資者建立穩健的理財觀念與基礎，減少因資訊過載或操作複雜所帶來的障礙。我們專注於「推薦」與「模擬試算」，不涉及交易操作，讓使用者能無壓力地學習與試算，並依照風險屬性找到最適合的投資組合。
            </div>
            <div v-if="page==='combination'">
                智能投資組合
            </div>
            <div v-if="page==='invest'">
                模擬投資試算
            </div>
            <div v-if="page==='article'">
                知識專欄
            </div>
            <div v-if="page==='personal'">
                個人化服務
            </div>
        </div>
    </div>
    

</main>
</template>

<style scoped>
main{
    font-family: 'GenRyuMin-M';
    margin: auto;
    margin-top: 5%;
    width: 80%;
}
.introduce{
    display: flex;
    width: 100%;
    border-radius: 15px;
    min-height: 800px;
}
.introduce button{
    font-family: 'GenRyuMin-B';
    display: block;
    border-radius: 15px 0 0 15px;
    background-color: #cfdde6;
    border: none;
    font-size: 16px;
    padding: 10%;
    margin-bottom: 10px;
    transition-duration:0.2s;
}
.introduce button:hover{
    color: rgb(100, 77, 77);
    padding-top: 20%;
    padding-bottom: 20%;
    
}
.introduce button.current{
    font-weight: bold;
    background-color: rgb(250, 232, 211);
    padding-top: 20%;
    padding-bottom: 20%;
}

.left{
    width: 20%;
    display: flex;
    border-radius: 15px;
    flex-direction: column;
}
.right{
    width: 80%;
    padding: 20px 35px;
    border-radius: 0 15px 15px 15px;
    background-color: rgb(243, 238, 232);

}

</style>