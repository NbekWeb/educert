<template>
    <Swiper
      :slides-per-view="1"
      :space-between="50"
      @swiper="onSwiper"
      @slideChange="onSlideChange"
    >
      <SwiperSlide v-for="i in 10" :key="i">
    <swipperCardVue/>
    </SwiperSlide>
    </Swiper>
  </template>
  
  <script setup>
  import swipperCardVue from '../cards/swipper-card.vue';
  import { ref } from 'vue';
  import { Swiper, SwiperSlide } from 'swiper/vue';
  import 'swiper/css';
  
  const onSwiper = (swiper) => {
    console.log(swiper);
  };
  
  const onSlideChange = () => {
    console.log('slide change');
  };
  </script>
  