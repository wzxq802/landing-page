<template>
  <div class="container relative w-full mx-auto overflow-hidden pl-14">
    <div class="flex justify-between items-center pl-10">
      <h2 class="font-bold text-4xl text-[#222]">Решения платформы</h2>
      <div class="flex justify-between items-center my-7 pr-24 space-x-2">
        <div ref="prevElRef" class="bg-white/80 hover:bg-white w-8 h-8 rounded-full shadow flex items-center justify-center">
          <span class="swiper-button-prev"></span>
        </div>
        <div ref="nextElRef" class="bg-white/80 hover:bg-white w-8 h-8 rounded-full shadow flex items-center justify-center">
          <span class="swiper-button-next"></span>
        </div>
      </div>
    </div>

    <swiper
      :modules="modules"
      :navigation="{
        prevEl: prevElRef,
        nextEl: nextElRef
      }"
      :slides-per-view="1.5"
      :space-between="16"
      :centered-slides="false"
      :breakpoints="breakpoints"
      class="w-full h-full"
    >
      <swiper-slide v-for="slide in sliderData" :key="slide.id" class="bg-gray-100 rounded-lg border border-gray-200 p-6">
        <div class="flex flex-row items-center justify-between gap-8 w-full">
          <div class="w-2/3">
            <h5 class="font-bold text-[#00B359] text-3xl">
              {{ slide.title }}
            </h5>
            <div class="text-xl mt-3 text-gray-800">
              {{ slide.description }}
            </div>
          </div>
          <div class="w-1/2 flex justify-end">
            <img :src="slide.image" :alt="slide.title" class="max-w-full h-auto object-contain">
          </div>
        </div>
      </swiper-slide>
    </swiper>
  </div>
</template>

<script lang="ts" setup>
import { sliders } from '@/shared/sliderMock';
import type { SliderData } from '@/shared/types/slider'

import { Swiper, SwiperSlide } from 'swiper/vue'
import { Navigation } from 'swiper/modules'
import 'swiper/css'
import 'swiper/css/navigation'
import { ref } from 'vue'

const prevElRef = ref(null)
const nextElRef = ref(null)
const modules = [Navigation]
const sliderData: SliderData[] = sliders

const breakpoints = {
  // 1 слайд на мобильных и планшетах
  320: {
    slidesPerView: 1,
    spaceBetween: 10
  },
  // 1.5 слайда на десктопах
  1024: {
    slidesPerView: 1.5,
    spaceBetween: 16
  }
}
</script>

<style>
.swiper {
  padding: 0 24px !important; 
}

/* Стили для десктопов (1.5 слайда) */
@media (min-width: 1024px) {
  .swiper-slide {
    width: 66.66% !important;
    margin-right: 16px;
  }
}

/* Стили для мобильных и планшетов (1 слайд) */
@media (max-width: 1023px) {
  .swiper-slide {
    width: 100% !important;
    margin-right: 0;
  }
}

.swiper-slide {
  transition: transform 0.3s ease;
}

.swiper-slide:not(.swiper-slide-active) {
  opacity: 0.7;
}

.swiper-button-prev,
.swiper-button-next {
  width: 32px;
  height: 32px;
  background: white;
  border-radius: 50%;
  box-shadow: 0 2px 8px rgba(0,0,0,0.1);
  position: static !important; 
  margin-top: 0 !important;
  margin-left: 0 !important;
  margin-right: 0 !important;
}

.swiper-button-prev::after,
.swiper-button-next::after {
  font-size: 14px;
  color: #00B359;
}
</style>