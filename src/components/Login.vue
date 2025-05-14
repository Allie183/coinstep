<script setup>
import { ref } from 'vue';

let page=ref("login"); //用PAGE紀錄響應式狀態
let change=function(clickpage){
    page.value=clickpage;
}
</script>

<template>
<main>
<div class="container">
    <div v-if="page==='login'">
        <form action="#">
            <h1>會員登入</h1>
            <input type="text" placeholder="Account" name="username" required="required"/>
            <input type="password" placeholder="Password" name="password" required="required"/>
            <button>登入</button>
        </form>
        <button class="p p2" :class="page==='res'?'current':''"  @click="change('res')">創建新帳戶</button>
        <button class="p">忘記密碼</button>
    </div>
    <div v-if="page==='res'">
        <form action="#">
            <h1>創立帳戶</h1>
            <input type="text" placeholder="Name" name="Name" required="required"/>
            <input type="email" placeholder="Email" name="email" required="required"/>
            <input type="password" placeholder="Password" name="password" required="required"/>
            <button>註冊</button>
        </form>
        <button class="p" :class="page==='login'?'current':''"  @click="change('login')">點擊以登入</button>
    </div>


</div>
</main>
</template>

<style scoped>
main{
  font-family: 'GenRyuMin-M';
  letter-spacing: 3px;
  line-height: 20px;
  margin: auto;
  width: 80%;

}
.container{
  background-color: #fff;
  border-radius: 10px;
  box-shadow: 0 14px 28px rgba(0, 0, 0, 0.25),
      0 10px 10px rgba(0, 0, 0, 0.22);
  position: relative;
  overflow: hidden;
  width: 700px;
  margin-top: 10%;
  padding: 8%;
  /* max-width: 100%; */
  min-height: 420px;

}
.p{
  color: #3f3527;
  border: none;
  margin-top: 30px;
  width: 49%;
  background-color: #ccb493;
  border-radius: 25px;
  font-family: 'GenRyuMin-M';
  font-size: 16px;
  letter-spacing: 3px;
  padding: 10px 35px;
  text-transform: uppercase;
  transition: transform 80ms ease-in;
}
.p2{
  margin-right: 2%;
}
.p:hover{
  background-color: #4e5c64;
  color: #ffffff;
}

.container form {
  background-color: #FFFFFF;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  height: 100%;
  text-align: center;
}
.container input {
  font-family: 'Mukta', sans-serif;
  background-color: #eee;
  border: none;
  border-radius: 5px;
  padding: 12px 15px;
  margin: 10px 0;
  width: 100%;
  font-size: 14px;
}
.container form button {
  border-radius: 25px;
  border: 1px solid #f7f7f7;
  background-color: #f8de9b;
  color: #3f3527;
  font-family: 'GenRyuMin-M';
  font-size: 16px;
  letter-spacing: 3px;
  padding: 10px 35px;
  width: 100%;
  text-transform: uppercase;
  transition: transform 80ms ease-in;
  margin-top: 25px;
}
.container form button:hover {
  background-color: #6a828f;
  color: #ffffff;
}

.container button:active {
  transform: scale(0.95);
}

.container button:focus {
  outline: none;
}

.container button.ghost {
  background-color: transparent;
  border-color: #FFFFFF;
}
</style>