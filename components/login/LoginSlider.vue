<script setup>
import { Swiper, SwiperSlide } from "swiper/vue";
import { Autoplay } from "swiper/modules";
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
{
    img:"/assets/images/png/slider-img-5.png",
},
];
</script>

<template>
  <div class="min-h-screen relative flex justify-center items-center">
    <div class="absolute z-[2]">
    <LoginForm/>
    </div>
     <swiper
      :slides-per-view="1"
      :loop="true"
      :autoplay="{
        delay: 2000,
        disableOnInteraction: false,
      }"
      :modules="[Autoplay]"
      class="h-screen"
    >
      <SwiperSlide v-for="(slide, index) in slideData" :key="index">
        <NuxtImg
          :src= "slide.img"
          :alt="'slide' + (index + 1)"
          class="w-full h-full object-cover"
        />
      </SwiperSlide>
    </swiper>
  </div>
</template>

