<template>
  <h1 style="padding-top: 24px">Swiperjs: render 10000 slides within 10000 divs</h1>
  <swiper :modules="[Virtual]" :virtual="true">
    <swiper-slide v-for="i in 10000" :key="i">
      <div>
        <div v-for="j in 10000">
          Slide {{ i }} + {{ j }}
        </div>
      </div>
    </swiper-slide>
  </swiper>
</template>

<script setup lang="ts">
// Import Swiper Vue.js components
import { Swiper as SwiperInstance, Virtual } from 'swiper';
import { Swiper, SwiperSlide } from 'swiper/vue';

// Import Swiper styles
import 'swiper/css';
</script>