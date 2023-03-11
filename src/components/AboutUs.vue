<template>
   <div class="about-us__row" id="aboutus">
      <div class="about-us__img">
         <img src="../assets/img/about-us-pizza.png" alt="photo pizza">
         <img class="fries" src="../assets/img/fries.png" alt="icon fries">
         <img class="pizza" src="../assets/img/pizza-icon.png" alt="icon pizza">
      </div>
      <div class="about-us__body">
         <div class="about-us__title">About us</div>
         <p class="about-us__text">In just a couple of years, we have opened 6 outlets in different cities: Kazan,
            Chelyabinsk, Ufa, Samara, Izhevsk, and in the future we plan to develop the network in other major cities of
            Russia.</p>
         <img class="group-pizza" src="../assets/img/group-pizza.png" alt="photo of pizza assortment">
         <p class="about-us__text">The kitchen of each point is at least: 400-500 sq. m. meters, hundreds of employees,
            smoothly performing work in order to receive / prepare / form / deliver customer orders on time.</p>
         <img class="arrow-to-pizza" src="../assets/img/arrow-title.svg" alt="arrow">
      </div>
   </div>
</template>

<script>

</script>

<style lang="scss" scoped>
.about-us__row {
   margin-bottom: 50px;
}

.about-us__img {
   margin: 0 auto 35px;
   width: 257px;
   height: 272px;
   position: relative;

   img {
      width: 100%;
      height: 100%;
   }

   .fries {
      width: 110px;
      height: 117px;
      position: absolute;
      bottom: -9px;
      left: -23px;
   }

   .pizza {
      width: 130px;
      height: 130px;
      position: absolute;
      top: -42px;
      right: -30px;
   }
}

.about-us__body {
   padding: 0 5%;

   .group-pizza {
      display: block;
      width: 268px;
      margin: 0 auto 28px;
   }

   .arrow-to-pizza {
      display: none;
   }
}

.about-us__title {
   font-weight: 800;
   font-size: 48px;
   line-height: 109.5%;
   color: #FFFFFF;
   margin-bottom: 28px;
}

.about-us__text {
   font-weight: 400;
   font-size: 14px;
   line-height: 136%;
   color: #A3A3A3;

   &:first-of-type {
      margin-bottom: 20px;
   }
}

@media (min-width: 630px) {
   .about-us__img {
      width: 330px;
      height: 334px;
   }

   .about-us__body {
      .group-pizza {
         width: 405px;
      }
   }

   .about-us__text {
      &:first-of-type {
         margin-bottom: 8px;
      }
   }
}

@media (min-width: 1000px) {
   .about-us__row {
      margin-bottom: 75px;
      padding: 0 5%;
      display: flex;
      flex-direction: row-reverse;
      justify-content: space-between;
   }

   .about-us__body {
      padding: 50px 0 0;
      flex: 0 1 460px;
      position: relative;

      .group-pizza {
         width: 100%;
      }

      .arrow-to-pizza {
         position: absolute;
         display: block;
         right: -120px;
         bottom: 256px;
         z-index: -2;
      }
   }

   .about-us__title {
      font-size: 69px;
   }

   .about-us__text {
      font-size: 20px;
   }

   .about-us__img {
      margin: 0;
      flex: 0 1 650px;
      height: 710px;

      img {
         width: 100%;
         height: 100%;
         object-position: 35px 0;
      }

      .fries {
         width: 203px;
         height: 216px;
         bottom: -9px;
         left: -23px;
      }

      .pizza {
         width: 237px;
         height: 237px;
         top: -67px;
         right: -49px;
      }
   }
}

@media (min-width: 1440px) {
   .about-us__row {
      width: 1440px;
      margin: 0 auto 75px;
   }
}
</style>