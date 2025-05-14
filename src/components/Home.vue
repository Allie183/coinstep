<script setup>

</script>

<template>
<main>
<div id="carouselExampleIndicators" class="carousel slide" data-bs-ride="carousel">
  <div class="carousel-indicators">
    <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="0" class="active" aria-current="true" aria-label="Slide 1"></button>
    <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="1" aria-label="Slide 2"></button>
    <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="2" aria-label="Slide 3"></button>
  </div>
  <div class="carousel-inner">
    <div class="carousel-item active">
      <img src="../assets/ad13.svg" class="d-block w-100" >
    </div>
    <div class="carousel-item">
      <img src="../assets/ad12.svg" class="d-block w-100" >
    </div>
    <div class="carousel-item">
      <img src="../assets/ad11.svg" class="d-block w-100" >
    </div>
  </div>
  <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide="prev">
    <span class="carousel-control-prev-icon" aria-hidden="true"></span>
    <span class="visually-hidden">Previous</span>
  </button>
  <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide="next">
    <span class="carousel-control-next-icon" aria-hidden="true"></span>
    <span class="visually-hidden">Next</span>
  </button>
</div>
<div class="feature">
    <h1>平台特色</h1>
    <div class="fcard">
        <div class="card1">
          <img src="../assets/ad14.png" >
            投資試算...
        </div>
        <div class="card1">
          <img src="../assets/ad15.svg">
            優化數據...
        </div>
        <div class="card1">
          <img src="../assets/ad17.jpg" >
            知識教育...
        </div>
    </div>
</div>
<div class="s">
    <div>
      <img src="../assets/ad4.png" class="simg">
    </div>
    <div class="s1">
      <h1>智能投資組合</h1>
      <h5>Intelligent Portfolio</h5>
      <p>透過演算法+投資組合最佳化技術產出智能投資組合，並依據市場情況動態調整投資組合權重。</p>
      <button>進入智能投資組合
        <img src="../assets/next.png" class="arrow">
      </button>
    </div>
</div>
<div class="s">
    <div class="s1">
      <h1>知識教育</h1>
      <h5>Knowledge and Education</h5>
      <p>提供您吸收新知與延伸學習專屬智庫，涵蓋股票、ETF、基金等主題，內容深入淺出，適合新手學習。</p>
      <button>
        進入知識教育
        <img src="../assets/next.png" class="arrow">
      </button>
    </div>
    <div>
      <img src="../assets/ad16.jpg" class="simg">
    </div>
</div>

</main>
</template>

<style scoped>
main{
    margin: auto;
    width: 100%;
    margin-top: 3.5%;

}
.carousel{
    width: 100%;

}
.carousel-item img{
    width: 100%;
    height: 650px;
    object-fit: cover;
    flex: 1;
 

}
.feature{
    width: 100%;
    justify-items: center;
    padding-top: 3%;
    padding-bottom: 5%;
    padding-left: 10%;
    padding-right: 10%;
    font-size: 24px;
    background-image: url(../assets/background.png);
}
.feature h1{
  font-family: 'GenRyuMin-B';
  font-weight: bold;
  margin-bottom: 50px;
}
.feature img{
  width: 200px;
}
.fcard{
    font-family: 'GenRyuMin-R';
    width: 100%;
    display: flex;
    flex-direction: row;
    text-align: center;
    justify-items: center;

}
.card1{
    width: auto;
    padding: 30px;
    display: flex;
    flex-direction: column;
    margin: auto;
    border-radius: 25px;
    border: #d4d3d2 solid 3px;
    background-color: rgb(255, 255, 255);
    
}
.s{
    width: 75%;
    margin: auto;
    display: flex;
    flex-direction: row;
    padding: 3%;
    font-family: 'GenRyuMin-R';
}
.s1{
    padding: 50px;
    margin: auto;
    
}
.s1 h1{
  font-family: 'GenRyuMin-M';

}
.s1 p{
  margin-top: 50px;
}
.s1 button{
  font-family: 'GenRyuMin-B';
  margin-top: 50px;
  padding: 20px 40px;
  border: none;
  background-color:#f8de9b;
  border-radius: 35px;
  transition-duration:0.3s;
}
.s1 button:hover{
  background-color: #f8de9ba0;
  margin-left: 10px;
}
.arrow{
  width: 15px;
}
.simg{
  width: 500px;
}
</style>