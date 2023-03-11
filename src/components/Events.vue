<template>
   <div class="events__body">
      <div class="events__title">Events</div>
      <p class="events__text">There are regular events in our pizzeria that will allow you to eat delicious food for a
         lower
         price!</p>
   </div>
   <div class="events__images" id="events">
      <div class="events__body-img">
         <div class="events__title">Events</div>
         <p class="events__text">There are regular events in our pizzeria that will allow you to eat delicious food for
            a
            lower
            price!</p>
      </div>
      <div class="events__img1 events__img">
         <img src="../assets/img/events/row1-1.png" alt="how we cooking">
         <span>HOW WE <br> COOKING</span>
         <button type="button">More</button>
      </div>
      <div class="events__img2 events__img">
         <img src="../assets/img/events/row1-2.png" alt="our blog">
         <span>OUR BLOG</span>
         <button type="button">More</button>
      </div>
      <div class="events__img-2row">
         <div class="events__img3 events__img">
            <img src="../assets/img/events/row2-1.png" alt="sale">
            <span>TWO PIZZA <br> FOR 1 PRICE</span>
            <button type="button">More</button>
            <img class="icon-becon" src="../assets/img/events/bacon.png" alt="becon">
         </div>
         <div class="events__img4 events__img">
            <img src="../assets/img/events/row2-2.png" alt="kitchen tour">
            <span>KITCHEN <br> TOUR</span>
            <button type="button">More</button>
            <img class="icon-buritto" src="../assets/img/events/buritto.png" alt="buritto">
         </div>
      </div>
      <div class="events__img5 events__img">
         <img src="../assets/img/events/row3-1.png" alt="profitable proposition">
         <span>FREE COFFEE <br> FOR 3 PIZZA</span>
         <button type="button">More</button>
         <img class="icon-coffee" src="../assets/img/events/coffee.png" alt="coffee">
      </div>
      <div class="events__img6 events__img">
         <img src="../assets/img/events/row3-2.png" alt="our instagram">
         <span>OUR <br> INSTAGRAM</span>
         <button type="button">More</button>
      </div>
      <div class="events__img7 events__img">
         <img src="../assets/img/events/row3-3.png" alt="where are you choose us?">
         <span>WHERE ARE <br> YOU CHOOSE <br> US?</span>
         <button type="button">More</button>
      </div>
   </div>
</template>

<script>

</script>

<style lang="scss" scoped>
.events__images {
   padding: 0 10% 50px;
   overflow-x: scroll;
   overflow-y: hidden;
   display: grid;
   grid-template-columns: repeat(3, minmax(229px, 1fr));
   grid-template-rows: repeat(3, 162px);
   grid-template-areas:
      "img1 img1-2 ."
      "img2 img2 img2"
      "img3-1 img3-2 img3-3";
   gap: 15px;

   &::-webkit-scrollbar {
      display: none;
   }

   img {
      width: 100%;
      height: 100%;
      border-radius: 30px;
   }

   .events__body-img {
      display: none;
   }

   .icon-becon,
   .icon-buritto,
   .icon-coffee {
      display: none;
   }
}

.events__body {
   padding: 0 5% 0 10%;
   text-align: right;
}

.events__title {
   font-weight: 800;
   font-size: 48px;
   line-height: 109.5%;
   color: #FFFFFF;
   margin-bottom: 28px;
}

.events__text {
   font-weight: 400;
   font-size: 14px;
   line-height: 136%;
   color: #A3A3A3;
   margin-bottom: 28px;
}

.events__img1 {
   grid-area: img1;
}

.events__img2 {
   grid-area: img1-2;
}

.events__img-2row {
   grid-area: img2;
   display: flex;
   gap: 15px;

   .events__img3,
   .events__img4 {
      width: 615px;
      height: 162px;
   }
}

.events__img5 {
   grid-area: img3-1;
}

.events__img6 {
   grid-area: img3-2;
}

.events__img7 {
   grid-area: img3-3;
}

.events__img {
   position: relative;

   span {
      position: absolute;
      top: 50px;
      left: 15px;
      font-weight: 500;
      font-size: 16px;
      line-height: 108.5%;
      color: #FFFFFF;
      text-transform: uppercase;
   }

   button {
      position: absolute;
      left: 15px;
      bottom: 25px;
      background: linear-gradient(261.69deg, #FF5D29 12.12%, #FE9C1C 86.72%);
      border-radius: 20px;
      font-weight: 500;
      font-size: 10px;
      line-height: 108.5%;
      color: #FFFFFF;
      padding: 7px 52px;

      &:hover {
         opacity: 0.8;
      }
   }
}

@media (min-width: 1000px) {
   .events__body {
      display: none;
   }

   .events__title {
      font-size: 69px;
      margin-bottom: 8px;
   }

   .events__text {
      font-size: 20px;
      margin-bottom: 0;
   }

   .events__images {
      position: relative;
      padding: 0 5% 75px;
      overflow-x: scroll;
      overflow-y: hidden;
      -ms-overflow-style: none;
      display: grid;
      grid-template-columns: repeat(3, minmax(367px, 1fr));
      grid-template-rows: repeat(3, 260px);
      grid-template-areas:
         "img1 img1-2 ."
         "img2 img2 img2"
         "img3-1 img3-2 img3-3";
      gap: 25px;

      .events__body-img {
         display: block;
         text-align: right;
         display: flex;
         flex-direction: column;
         justify-content: flex-end;
      }

      .icon-becon,
      .icon-buritto,
      .icon-coffee {
         display: block;
      }
   }

   .events__img-2row {
      grid-area: img2;
      display: flex;
      gap: 25px;

      .events__img3,
      .events__img4 {
         width: 615px;
         height: 260px;
      }

      .events__img3 {
         position: relative;

         .icon-becon {
            position: absolute;
            top: -123px;
            left: -102px;
            width: 245px;
            height: 257px;
         }
      }

      .events__img4 {
         position: relative;

         .icon-buritto {
            position: absolute;
            width: 258px;
            height: 278px;
            top: 0;
            right: -112px;
         }
      }
   }

   .events__img5 {
      position: relative;

      .icon-coffee {
         position: absolute;
         width: 200px;
         height: 200px;
         bottom: -72px;
         left: -83px;
      }
   }

   .events__img {
      span {
         top: 72px;
         left: 22px;
         font-size: 25px;
      }

      button {
         left: 22px;
         bottom: 40px;
         font-size: 16px;
         padding: 11px 82px;
      }
   }
}

@media (min-width: 1440px) {
   .events__images {
      max-width: 1440px;
      margin: 0 auto;
   }
}
</style>
