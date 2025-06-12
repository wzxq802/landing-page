<template>
  <section class="advantages py-5 md:py-7 my-5 md:my-14">
    <div class="container mx-auto px-4 md:px-6">
      <div class="flex flex-col lg:flex-row gap-8 lg:gap-12 xl:gap-16">
        <div class="lg:order-1 flex justify-center">
          <img 
            src="@/assets/images/advantages_hero.png" 
            alt="house" 
            class="w-full max-w-full md:max-w-[90%] lg:max-w-[793px] lg:pl-14"
          >
        </div>
        <div class="lg:order-2">
          <h2 class="font-bold text-2xl sm:text-3xl md:text-4xl text-[#222] mb-5 md:mb-7">
            Преимущества платформы
          </h2>
          <ul class="space-y-3 md:space-y-4">
            <li 
              v-for="item in advantagesData" 
              :key="item.id" 
              class="flex items-start gap-3 md:gap-4"
            >
              <img 
                src="@/assets/images/check.png" 
                alt="check" 
                class="w-5 h-5 mt-0.5 flex-shrink-0"
              >
              <span class="text-base md:text-lg">{{ item.title }}</span>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </section>
</template>

<script lang="ts" setup>
import { advantages } from '@/shared/advantagesMock'
import type { AdvantagesData } from '@/shared/types/advantages'
const advantagesData: AdvantagesData[] = advantages
</script>