<template>
   <div class="preview__row">
      <div class="preview__img">
         <img src="../assets/img/preview-pizza.png" alt="photo pizza">
         <img class="fries" src="../assets/img/fries.png" alt="icon fries">
         <img class="pizza" src="../assets/img/pizza-icon.png" alt="icon pizza">
      </div>
      <div class="preview__body">
         <div class="preview__title">The Fastest <br> Pizza<span><img src="../assets/img/lightning.svg"
                  alt="lighting svg"></span>Delivery
            <img class="title-arrow" src="../assets/img/arrow-title.svg" alt="arrow">
         </div>
         <p class="preview__text">We will deliver juicy pizza for your family in 30 minutes, if the courier is late -
            <span>pizza is free!</span>
         </p>
         <button class="preview__button" @click="changeBtnColor" type="button">
            <span :class="{ active: isActive }"> To order </span>
            <span :class="{ active: !isActive }"> Pizza - Menu </span>
         </button>
         <div class=" preview__cooking">
            <p>Cooking process:</p>
            <div class="cooking__img">
               <img class="full-img-pizza" src="../assets/img/cooking-pizza.png" alt="cooking pizza">
               <img class="icon-play" src="../assets/img/play.svg" alt="icon play">
               <img class="icon-play-ellipse" src="../assets/img/play-ellipse.svg" alt="icon play ellipse">
            </div>
         </div>
         <img class="arrow-from-button" src="../assets/img/arrow-from-button.svg" alt="arrow from button">
      </div>
   </div>
</template>

<script>
export default {
   data() {
      return {
         isActive: true,
      }
   },
   methods: {
      changeBtnColor() {
         this.isActive = !this.isActive;
      }
   }
}
</script>

<style lang="scss" scoped>
@import '../assets/vars';

.preview__row {
   overflow: hidden;
   padding: 100px 0;
}

.preview__img {
   width: 243px;
   height: 365px;
   margin: 0 auto 30px;
   position: relative;

   img {
      width: 100%;
   }

   .fries,
   .pizza {
      position: absolute;
   }

   .fries {
      left: -42px;
      bottom: 0;
      width: 110px;
      height: 117px;
   }

   .pizza {
      right: -46px;
      top: -46px;
      width: 130px;
      height: 130px;
   }
}

.preview__body {
   padding: 0 5%;

   .arrow-from-button {
      display: none;
   }
}

.preview__title {
   font-weight: 800;
   font-size: 34px;
   line-height: 109.5%;
   color: #FFFFFF;
   margin-bottom: 24px;

   .title-arrow {
      display: none;
   }

   >span {
      margin: 0 5px 0 10px;
      display: inline-block;
      width: 35px;
      height: 40px;
      position: relative;

      img {
         width: 100%;
         position: absolute;
         top: 5px;
         left: 0;
      }
   }
}

.preview__text {
   font-weight: 400;
   font-size: $fontSize;
   line-height: 151.5%;
   color: #A3A3A3;
   margin-bottom: 32px;

   >span {
      color: #FFFFFF;
   }
}

.preview__button {
   border-radius: 71px;
   border: 2px solid #FF6939;
   background: transparent;
   background: linear-gradient(261.69deg, #FF6432 12.12%, #FFA228 86.72%);
   -webkit-background-clip: text;
   -webkit-text-fill-color: transparent;
   background-clip: text;
   margin-bottom: 32px;
   font-size: 16px;

   span {
      display: inline-block;

      &:nth-child(1) {
         padding: 12px 14px 12px 25px;
      }

      &:nth-child(2) {
         padding: 12px 25px 12px 14px;
      }

      &.active {
         border-radius: 71px;
         padding: 12px 45px;
         background: linear-gradient(261.48deg, #FE9C1C -17.13%, #FF5E2A 86.76%);
         -webkit-text-fill-color: #FFFFFF;
      }
   }
}

.preview__cooking {
   p {
      font-size: $fontSize;
      line-height: 136%;
      color: #A3A3A3;
   }
}

.cooking__img {
   position: relative;
   width: 330px;
   height: 220px;

   .full-img-pizza {
      position: relative;
      top: -14px;
      left: -29px;
   }

   .icon-play,
   .icon-play-ellipse {
      position: absolute;
   }

   .icon-play {
      top: 93px;
      left: 126px;
      z-index: 3;
   }

   .icon-play-ellipse {
      top: 36px;
      left: 60px;
   }
}

@media (min-width: 1000px) {
   .preview__row {
      display: flex;
      justify-content: space-between;
      flex-direction: row-reverse;
      padding: 50px 5% 75px;
   }

   .preview__img {
      width: 456px;
      height: 684px;
      margin: 0;

      .fries {
         left: -83px;
         bottom: -16px;
         width: 213px;
         height: 226px;
      }

      .pizza {
         right: -85px;
         top: -88px;
         width: 252px;
         height: 252px;
      }
   }

   .preview__body {
      flex: 0 0 450px;
      display: flex;
      flex-direction: column;
      padding: 85px 0 0;
      position: relative;

      .arrow-from-button {
         display: block;
         width: 120px;
         position: absolute;
         bottom: -61px;
         right: -12px;
      }
   }

   .preview__title {
      width: 400px;
      font-size: 48px;
      position: relative;

      .title-arrow {
         display: block;
         width: 88px;
         position: absolute;
         top: 15px;
         right: 0;
      }
   }

   .preview__text {
      width: 425px;
      font-size: 18px;
   }

   .preview__button {
      order: 10;
      align-self: flex-start;
      font-size: 18px;

      span {
         &:nth-child(1) {
            padding: 17px 14px 17px 25px;
         }

         &:nth-child(2) {
            padding: 17px 25px 17px 14px;
         }

         &.active {
            padding: 17px 50px;
         }
      }
   }

   .preview__cooking {
      p {
         font-size: 18px;
      }
   }

   .cooking__img {
      margin-bottom: 45px;
   }
}

@media (min-width: 1440px) {
   .preview__row {
      max-width: 1440px;
      margin: 0 auto;
   }
}
</style>