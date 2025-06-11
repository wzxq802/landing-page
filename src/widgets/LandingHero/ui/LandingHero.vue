<template>
  <section class="hero flex justify-center items-center mt-9">
    <div class="max-w-xl">
      <h1 class="font-bold text-5xl text-[#222] mb-7">{{ title }}</h1>
      <p class="text-xl text-[#222] mb-7">{{ subtitle }}</p>
      <button class="rounded-xl px-8 py-4 block max-w-[341px] w-[100%] bg-[#00b359] hover:bg-[#007439] text-[#fff]">Начать проект</button>
    </div>
    <div>
      <img class="block max-w-[678px]" src="@/assets/images/hero-image.png" alt="house">
    </div>
  </section>
</template>

<script lang="ts" setup>
import { heroData } from '@/shared/heroMock'

const { title, subtitle } = heroData
</script>

