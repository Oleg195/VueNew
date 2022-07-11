<template >
<div>
 <div class="container">

    <div class="slider">
      <div class="slider__wrapper">
        <div class="slider__items">
          <div class="slider__item">
           
            1
          </div>
          <div class="slider__item">
            <!-- Контент 2 слайда -->
            2
          </div>
          <div class="slider__item">
            <!-- Контент 3 слайда -->
            3
          </div>
          <div class="slider__item">
            <!-- Контент 4 слайда -->
            4
          </div>
          <div class="slider__item">
            <!-- Контент 5 слайда -->
            5
          </div>
        </div>
      </div>
      <a href="#" class="slider__control" data-slide="prev"></a>
      <a href="#" class="slider__control" data-slide="next"></a>
      <ol class="slider__indicators">
        <li data-slide-to="0"></li>
        <li data-slide-to="1"></li>
        <li data-slide-to="2"></li>
        <li data-slide-to="3"></li>
        <li data-slide-to="4"></li>
      </ol>
    </div>

  </div>


      <div class="flex">
        
        <div class="text">
      <h1 class="welcome">Welcome!</h1>
        <ul><h2 class="why">why us?</h2>
  <li class="spisok">fast feedback</li>
  <li class="spisok">high quality</li>
  <li class="spisok">fast delivery</li>
  <li class="spisok"><h2>best for customers ;)</h2></li>
</ul>
</div>
        <img class="golova" src="./images/Снимок экрана (8).png" alt="">
    </div>
    </div>
</template>

<script>
    document.addEventListener('DOMContentLoaded', function () {
      const slider = new ChiefSlider('.slider', {
        loop: true,
        autoplay: true,
        interval: 7000,
      });
    });
</script>


<style scoped>
 *,
    *::before,
    *::after {
      box-sizing: border-box;
    }
.container {
      max-width: 700px;
      margin: 0 auto;
    }

    .slider__container {
      padding-left: 0;
      padding-right: 0;
    }

    .slider__items {
      counter-reset: slide;
    }

    .slider__item {
      -webkit-box-flex: 0;
      -ms-flex: 0 0 100%;
      flex: 0 0 100%;
      max-width: 100%;
      counter-increment: slide;
      height: 250px;
      position: relative;
    }

    .slider__item::before {
      content: counter(slide) "/5";
      position: absolute;
      top: 10px;
      right: 20px;
      color: #fff;
      font-style: italic;
      font-size: 32px;
      font-weight: bold;
      display: block;
    }

    .slider__item:nth-child(1) {
      background-color: #f44336;
    }

    .slider__item:nth-child(2) {
      background-color: #9c27b0;
    }

    .slider__item:nth-child(3) {
      background-color: #3f51b5;
    }

    .slider__item:nth-child(4) {
      background-color: #03a9f4;
    }

    .slider__item:nth-child(5) {
      background-color: #4caf50;
    }

.menu{ 
    background-color: #ffffff;;
    /* height: 75px;
    display: flex;
    align-items: center;
    justify-content: space-around; */
    /* box-shadow: rgb(44 85 146) 0px 19px 38px -29px inset; */
}
.flex{
 display: flex;
  flex-wrap: wrap;
  justify-content: flex-end;
  align-items: center;
}
.text{
  width: 25%;
  text-align: center;
  font-size: initial;
}
.text li{
  text-decoration: none;
  list-style-type: none;
  font-size: 150%;
}
.welcome {
  font-size: 365%;
  height: 0%;
}

.golova{
  width: 59%
}
.logo{
  display: flex;
  justify-content: center;
  font-size: 222%;
  align-items: center;
  margin: 1%;
  height: 10px;
}
   
@keyframes gorod{0%{background-position-x:0%}100%{background-position-x:96% ;}}
</style>