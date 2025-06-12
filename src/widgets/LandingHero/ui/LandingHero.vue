<template>
  <section class="hero flex flex-col-reverse lg:flex-row items-center justify-center gap-8 mt-9 mb-28 px-4 sm:px-6">
    <div class="container max-w-xl text-center lg:text-left">
      <h1 class="font-bold text-3xl sm:text-4xl lg:text-5xl text-[#222] mb-5 sm:mb-6 lg:mb-7">{{ title }}</h1>
      <p class="text-base sm:text-lg lg:text-xl text-[#222] mb-5 sm:mb-6 lg:mb-7">{{ subtitle }}</p>
      <button class="rounded-xl px-8 py-4 w-full max-w-[341px] mx-auto lg:mx-0 bg-[#00b359] hover:bg-[#007439] text-white">
        Начать проект
      </button>
    </div>
    <div class="w-full max-w-[778px] px-4 sm:px-0">
      <img class="w-full h-auto" src="@/assets/images/hero-image.png" alt="house" />
    </div>
  </section>
</template>

<script lang="ts" setup>
import { heroData } from '@/shared/heroMock'

const { title, subtitle } = heroData
</script>
