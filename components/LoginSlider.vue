<script setup>
import { Swiper, SwiperSlide } from "swiper/vue";
import { Autoplay, EffectFade } from "swiper/modules";
import "swiper/css";
 const slideData=[
{
    img:"/assets/images/png/slider-img-1.png",
},
{
    img:"/assets/images/png/slider-img-2.png",
},
{
    img:"/assets/images/png/slider-img-3.png",
},
{
    img:"/assets/images/png/slider-img-4.png",
},
];
</script>

<template>
  <div class="min-h-screen relative">
     <swiper
      :slides-per-view="1"
      :loop="true"
      :autoplay="{
        delay: 1500,
        disableOnInteraction: false,
      }"
      effect="fade"
      :modules="[Autoplay, EffectFade]"
      class="h-screen"
    >
      <SwiperSlide v-for="(slide, index) in slideData" :key="index">
        <NuxtImg
          :src= "slide.img"
          :alt="'slide' + (index + 1)"
          class="absolute top-0 left-0 w-full h-full object-cover"
        />
      </SwiperSlide>
    </swiper>
  </div>
</template>

