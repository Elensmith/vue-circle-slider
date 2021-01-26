<template>
  <div class="circle-slider">
    <h1 class="circle-slider__header">шесть факторов профессиональной защиты</h1>
      <div class="circle-slider__wrapper">
        <img 
        v-touch:swipe.left="touchHandlerLeft"
        v-touch:swipe.right="touchHandlerRight"
        src="@/assets/hexagon.svg" alt="" class="circle-slider__hexagon" />
        <img src="@/assets/hand.svg" alt="" class="circle-slider__hand" />
        <ul class="circle-slider__lists">
          <li class="circle-slider__list circle-slider__list_one circle-slider__list_on" id="1">ПОДХОДИТ ДЛЯ HI_TECH МАТЕРИАЛОВ_</li>
          <li class="circle-slider__list circle-slider__list_two " id="2">ЗАЩИТА БЕЛОГО ЦВЕТА / <br>ТЕХНОЛОГИЯ EXTRA WHITE_</li>
          <li class="circle-slider__list circle-slider__list_three" id="3">ЕВРОПЕЙСКИЕ ИННОВАЦИИ_</li>
          <li class="circle-slider__list circle-slider__list_four" id="4">_СОЗДАН ДЛЯ РОССИИ / <br>РАЗРАБОТАН ДЛЯ ЭКСТРЕМАЛЬНЫХ УСЛОВИЙ</li>
          <li class="circle-slider__list circle-slider__list_five" id="5">_ЭКСПЕРТИЗА / <br>СОБСТВЕННЫЕ <br>НАУЧНЫЕ РАЗРАБОТКИ</li>
          <li class="circle-slider__list circle-slider__list_six" id="6">_УНИКАЛЬНОСТЬ / <br>ЗАПАТЕНТОВАННЫЕ ТЕХНОЛОГИИ</li>
        </ul>
      </div>

  </div>
</template>

<script>
  export default {
    created () {
      this.position = 1;
    },

    methods: {
      touchHandlerLeft(e) {
   
        let hexagon = document.querySelector('.circle-slider__hexagon');
        let animation = hexagon.animate([
          {transform: 'rotate(60deg)'},
          {transform: 'rotate(0deg)'}
        ], 500);
        animation.addEventListener('finish', function() {
          hexagon.style.transform = 'rotate(0deg)';
        });
        document.getElementById(this.position).classList.remove("circle-slider__list_on");
        if (this.position >= 6){
          console.log(this.position)
          this.position = 1;
        } else if (this.position < 6) {
          this.position += 1;
        }
        document.getElementById(this.position).classList.add("circle-slider__list_on");
        console.log(e);
      },

      touchHandlerRight(e) {
        console.log(e);
        let hexagon = document.querySelector('.circle-slider__hexagon');
        let animation = hexagon.animate([
          {transform: 'rotate(0deg)'},
          {transform: 'rotate(60deg)'}
        ], 500);
        animation.addEventListener('finish', function() {
          hexagon.style.transform = 'rotate(60deg)';
        });
        document.getElementById(this.position).classList.remove("circle-slider__list_on");
         if (this.position <= 1){
          console.log(this.position)
          this.position = 6;
        } else if (this.position > 1) {
          this.position -= 1;
        }
        document.getElementById(this.position).classList.add("circle-slider__list_on");
      }
    }
  }

</script>
<style scoped>

  .circle-slider__hand {
    display: none;
  }
  .circle-slider__wrapper {
    overflow-y: hidden;
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
    top: 88%;
    left: 7%;
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

  .circle-slider__list {
    margin-left: auto;
    margin-right: auto;
    top: 120px;
    left: 0;
    right: 0;
    text-align: center;
    font-size: 18px;
    display: none;
  }

  .circle-slider__list_on {
    display: inline-block;
  }
  
  .circle-slider__wrapper {
    position: inherit;
    margin: 90px auto;
    max-width: 400px;
    min-width: 320px;
  }
  .circle-slider__hexagon {
    max-width: 100%;
    
  }
   .circle-slider__hand {
    position: absolute;
    left: 47%;
    top: 46%;
    display: inline-block;
    animation: 2s linear 4 hand;
  }

  @keyframes hand {
    0% {
      transform: translateX(100%);
    }
    100% {
      transform: translateX(-100%);
    }
  }

}

</style>