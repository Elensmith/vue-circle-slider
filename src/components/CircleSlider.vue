<template>
  <div class="circle-slider">
    <h1 class="circle-slider__header">шесть факторов профессиональной защиты</h1>
      <div class="circle-slider__wrapper">
        <img src="@/assets/hexagon.svg" alt="" class="circle-slider__hexagon" />
        <ul class="circle-slider__lists">
          <li class="circle-slider__list circle-slider__list_one">ПОДХОДИТ ДЛЯ HI_TECH МАТЕРИАЛОВ_</li>
          <li class="circle-slider__list circle-slider__list_two">ЗАЩИТА БЕЛОГО ЦВЕТА / <br>ТЕХНОЛОГИЯ EXTRA WHITE_</li>
          <li class="circle-slider__list circle-slider__list_three">ЕВРОПЕЙСКИЕ ИННОВАЦИИ_</li>
          <li class="circle-slider__list circle-slider__list_four">_СОЗДАН ДЛЯ РОССИИ / <br>РАЗРАБОТАН ДЛЯ ЭКСТРЕМАЛЬНЫХ УСЛОВИЙ</li>
          <li class="circle-slider__list circle-slider__list_five">_ЭКСПЕРТИЗА / <br>СОБСТВЕННЫЕ <br>НАУЧНЫЕ РАЗРАБОТКИ</li>
          <li class="circle-slider__list circle-slider__list_six">_УНИКАЛЬНОСТЬ / <br>ЗАПАТЕНТОВАННЫЕ ТЕХНОЛОГИИ</li>
        </ul>
      </div>

  </div>
</template>

<style scoped>
  .circle-slider {
  }
  .circle-slider__wrapper {
    overflow-y: hidden;
    /* display: flex;  
    align-content: center; */
   position: relative;
   margin: auto;
   max-width: 1200px;
   min-width: 1200px;
  }
  .circle-slider__header {
    color: white;
    text-align: left;
    margin-left: 111px;
    font-size: 28px;
    font-weight: bold;
    max-width: 500px;
  }
  
  .circle-slider__list {
    position: absolute;
    color: white;
    font-size: 21px;
    font-weight: bold;
  }
  .circle-slider__lists {
    list-style-type: none;
  }
  .circle-slider__list_one {
    top: 0;
    left: 50%;
  }
  .circle-slider__list_two {
    text-align: left;
    top: 26%;
    left: 63%;
  }
  .circle-slider__list_three {
    top: 65%;
    left: 63%;
  }
  .circle-slider__list_four {
    text-align: right;
    top: 92%;
    left: 5%;
  }
  .circle-slider__list_five {
    text-align: right;
    top: 60%;
    left: 14%;
  } 
  .circle-slider__list_six {
  text-align: right;
  top: 26%;
  left: 4%;
  }
  @media screen and (max-width: 426px) {
  .circle-slider__header {
    margin: auto;
    font-size: 20px;
    font-weight: bold;
    max-width: 312px;
  }
  .circle-slider__lists{
   display: none;
  }
  .circle-slider__wrapper {
    margin: 90px auto;
    max-width: 400px;
    min-width: 320px;
  }
  .circle-slider__hexagon {
    max-width: 300px;
    max-height: 300px;
  }
}

</style>