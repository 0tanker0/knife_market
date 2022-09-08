<template>
  <swiper class="slider"
    :slides-per-view="1"
    :modules="modules"
    effect="fade"
    :loop="true"
    navigation
    :pagination="{clickable: true, dynamicBullets: true}"
    grab-cursor
    >
    
    <swiper-slide>
      <div>
        <img src="../assets/images/kasumi/compressed/KISARAGI.webp"
          class="sl_photo">
        <h3 class="kisagari">KISAGARI</h3>
        <h4 class="s_kisagari">Авторский нож
          <br> Dew Hara
          <br> Япония
        </h4>
      </div>
    </swiper-slide>

    <swiper-slide>
      <div>
        <img src="../assets/images/kasumi/compressed/LEPREMIER.webp"
             class="sl_photo">

        <h3 class="premier">LE PREMIER</h3>
        <h4 class="premier stext">Профессиональная серия
          <br> кухнонных ножей
          <br> Sakai Kohj
          <br> Япония
        </h4>
      </div>
    </swiper-slide>

    <swiper-slide>
      <div>
        <img src="../assets/images/kasumi/compressed/MINA.webp"
             class="sl_photo">
        <h3 class="mina">MINA</h3>
        <h4 class="s_mina">Авторский нож
          <br> Dew Hara
          <br> Япония
        </h4>
      </div>
    </swiper-slide>

  </swiper>
</template>

<script>
import {Navigation, Pagination, Scrollbar, A11y, Virtual, EffectFade} from 'swiper';
import {Swiper, SwiperSlide} from "swiper/vue";

import "swiper/css"
import 'swiper/css/bundle'

export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Slider",
  components: {
    Swiper, SwiperSlide
  },
  data (){
    return{
      images:[
          {id: 1, name: "../assets/images/kasumi/compressed/KISARAGI.jpg", main_text: ''},
          {id: 2, name: "../assets/images/kasumi/compressed/MINA.jpg"},
          {id: 3, name: "../assets/images/kasumi/compressed/LEPREMIER.jpg"}
      ]
    }
  },
  setup () {
    return {
      modules: [Navigation, Pagination, Scrollbar, A11y, Virtual, EffectFade],
    };
  }
}
</script>

<style scoped>
h3 {
  color: black;
  position: absolute;
  top: 15px;
  margin-top: 35%;
  margin-left: 20%;
}
h4 {
  color: black;
  position: absolute;
  top: 10px;
  margin-top: 40%;
  margin-left: 20%;
}
.premier {
  margin-left: 80%;
  margin-top: 22%;
}
.stext {
  margin-top: 25%;
}
.sl_photo{
  height: 1024px;
  width: 2048px;
}
.mina{
  color: black;
  position: absolute;
  top: 15px;
  margin-top: 36%;
  margin-left: 20%;
}
.kisagari{
  color: black;
  position: absolute;
  top: 15px;
  margin-top: 35%;
  margin-left: 20%;
}
@media screen and (max-width: 1800px) {
  .premier{
    margin-top: 25%;
  }
  .stext{
    margin-top: 28%;
  }
  .mina{
    margin-top: 39%;
  }
  .s_mina{
    margin-top: 42%;
  }
  .kisagari{
    margin-top: 38%;
  }
  .s_kisagari{
    margin-top: 41%;
  }
}
@media screen and (max-width: 1600px) {
  .premier{
    margin-top: 28%;
  }
  .stext{
    margin-top: 31%;
  }
  .mina{
    margin-top: 42%;
  }
  .s_mina{
    margin-top: 45%;
  }
  .kisagari{
    margin-top: 41%;
  }
  .s_kisagari{
    margin-top: 44%;
  }
}
@media screen and (max-width: 1400px) {
  .premier{
    margin-top: 31%;
  }
  .stext{
    margin-top: 34%;
  }
  .mina{
    margin-top: 45%;
  }
  .s_mina{
    margin-top: 48%;
  }
  .kisagari{
    margin-top: 44%;
  }
  .s_kisagari{
    margin-top: 47%;
  }
}
@media screen and (max-width: 1200px) {
  .premier{
    margin-top: 34%;
  }
  .stext{
    margin-top: 37%;
  }
  .mina{
    margin-top: 60%;
  }
  .s_mina{
    margin-top: 65%;
  }
  .kisagari{
    margin-top: 53%;
  }
  .s_kisagari{
    margin-top: 56%;
  }
}
@media screen and (max-width: 1000px) {
  .premier{
    margin-top: 37%;
  }
  .stext{
    margin-top: 40%;
  }
  .mina{
    margin-top: 70%;
  }
  .s_mina{
    margin-top: 75%;
  }
  .kisagari{
    margin-top: 65%;
  }
  .s_kisagari{
    margin-top: 70%;
  }
}
@media screen and (max-width: 800px) {
  .premier{
    margin-top: 40%;
  }
  .stext{
    margin-top: 43%;
  }
  .mina{
    margin-top: 75%;
  }
  .s_mina{
    margin-top: 80%;
  }
  .kisagari{
    margin-top: 70%;
  }
  .s_kisagari{
    margin-top: 75%;
  }
}
</style>