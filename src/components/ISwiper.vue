<template>
  <h1 style="padding-top: 24px">Swiperjs with {{ obj.slides }} slides, {{ obj.images }} images and {{ obj.components }}
    components</h1>
  <swiper :modules="[Virtual, Keyboard]" :virtual="true" :keyboard="true">
    <swiper-slide v-for="i in obj.slides" :key="i">
      <div>
        <div style="display: flex; flex-wrap: wrap;">
          <img v-for="j in obj.images" :src="`https://picsum.photos/30/30?q=${i}${j}`" width="30" height="30">
        </div>

        <IItem v-for="j in obj.components">
          Slide {{ i }} + {{ j }}
        </IItem>
      </div>
    </swiper-slide>
  </swiper>
</template>

<script setup lang="ts">
import { Virtual, Keyboard } from 'swiper'
import { Swiper, SwiperSlide } from 'swiper/vue'
import IItem from './IItem.vue'

import 'swiper/css'

const obj = {
  slides: 10000,
  images: 100,
  components: 10000
}
</script>