<script setup>
import { ref } from 'vue';
import Home from './Home.vue';
import Main from './Main.vue';
import Combination from './Combination.vue';
import Invest from './Invest.vue';
import Article from './Article.vue';
import Login from './Login.vue';

let page=ref("home"); //用PAGE紀錄響應式狀態,預設是home
let change=function(clickpage){
    page.value=clickpage;
}
</script>

<template>
  <header class="sticky">
      <nav>
        <div class="container">
          <div class="left">
          <a :class="page==='home'?'current':''"  @click="change('home')"><img class="logo" src="../assets/coin.png " >
              CoinStep 投資新手村
          </a>
          </div>
          <div class="right">
            <ul class="nav_center">
              <li :class="page==='main'?'current':''"  @click="change('main')"><a>新手村指南</a></li>
              <li :class="page==='combination'?'current':''"  @click="change('combination')"><a>推薦組合</a></li>
              <li :class="page==='invest'?'current':''"  @click="change('invest')"><a>投資試算</a></li>
              <li :class="page==='article'?'current':''"  @click="change('article')"><a>知識專欄</a></li>
              <li :class="page==='login'?'current':''"  @click="change('login')">
                <div class="dropdown">
                  <a>會員專區</a>
                  <div class="dropdown-content">
                    <a href="#">會員中心</a>
                    <a href="#">推播通知</a>
                    <a href="#">收藏/追蹤</a>
                    <a href="#">帳戶設定</a>
                    <a href="#">登出</a>
                  </div>
                </div>
              </li>
            </ul>
        </div>
        </div>
      </nav>
  </header>
  <main>
    <Home v-if="page==='home'"></Home>
    <Main v-if="page==='main'"></Main>
    <Combination v-if="page==='combination'"></Combination>
    <Invest v-if="page==='invest'"></Invest>
    <Article v-if="page==='article'"></Article>
    <Login v-if="page==='login'"></Login>
  </main>
</template>

<style scoped>

/* 導覽列 */
header {
  width: 100%;
  height: 8%;
  font-family: 'GenRyuMin-B';
  position: fixed;
  top: 0;
  justify-content: space-between;
  align-items: center;
  z-index: 1000;
  transition: 0.4s;
  opacity: 0;
}

header.sticky {
  background: white;
  border-bottom: 1px solid rgb(218, 218, 218);
  opacity: 1;

}
a{
  cursor: pointer;
}
.logo {
  width: 20px;
  cursor: pointer;
}
.container{
  display: flex;
  padding-top: 15px;
  padding-left: 3%;
  padding-right: 5%;
  width: 100%;

}
.left{
  width: 30%;

}
.right{
  width: 70%;
}
.nav_center {
  list-style: none;
  display: flex;
  align-items: center;
  justify-content: center;

}

.nav_center li {
  display: inline-block;
  margin: 0px 35px;
  cursor: pointer;
  border-bottom: 0px solid #f7e5c4;
}
.nav_center li:hover{
  border-bottom: 5px;
}
.nav_center li a {
  transition: all 0.3s ease 0s;
  cursor: pointer;
}

.nav_center li a:hover {
  color: #878787;
}


nav,
ul,
li,
a {
  color: black;
  font-size: 17px;
  text-decoration: none;
  letter-spacing: 1px;
}


.nav_center li.current{
    font-weight: bold;
    border-bottom: #f7e5c4 solid 5px;
    
}
.dropdown {
  position: relative;
  display: inline-block;
  vertical-align: top;
}
.dropdown-content {
  display: none;
  position: absolute;
  margin-left: -20px;
  background-color: #f9f9f9;
  text-align: center;
  min-width: 180px;
  border-radius: 15px;
  box-shadow: 0px 8px 16px 0px rgba(0, 0, 0, 0.2);
  z-index: 1;
}

.dropdown-content a {
  color: black;
  padding: 12px 12px;
  text-decoration: none;
  display: block;
  font-size: 16px;
  border-radius: 15px;
}

.dropdown-content a:hover {
  background-color: #f1f1f1
}

.dropdown:hover .dropdown-content {
  display: block;
}

</style>
