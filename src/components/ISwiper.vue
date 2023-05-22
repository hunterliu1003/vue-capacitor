<template>
  <h1 style="padding-top: 24px">Swiperjs: render 10000 slides within 10000 divs</h1>
  <swiper :modules="[Virtual, Keyboard]" :virtual="true" :keyboard="true">
    <swiper-slide v-for="i in 10000" :key="i">
      <ISlide>
        <div v-for="j in 10000">
          Slide {{ i }} + {{ j }}
        </div>
      </ISlide>
    </swiper-slide>
  </swiper>
</template>

<script setup lang="ts">
import { Virtual, Keyboard } from 'swiper'
import { Swiper, SwiperSlide } from 'swiper/vue'
import ISlide from './ISlide.vue'

import 'swiper/css'
</script>