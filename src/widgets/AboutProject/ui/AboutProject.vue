<template>
  <section
    id="about"
    class="about bg-[url('/src/assets/images/about-project-bg.png')] bg-cover h-auto py-12 lg:h-[486px] flex items-center"
  >
    <div class="container mx-auto px-4 sm:px-6">
      <div class="max-w-3xl lg:pl-24">
        <h2 class="font-bold text-2xl sm:text-3xl lg:text-4xl text-white mb-5 sm:mb-6 lg:mb-7">
          {{ about.title }}
        </h2>
        <p class="text-white text-base sm:text-lg mb-5 sm:mb-6 lg:mb-7">
          {{ about.description }}
        </p>
        <div class="grid grid-cols-1 lg:grid-cols-3 gap-4 lg:gap-x-6">
          <div
            v-for="(item, id) in about.items"
            :key="id"
            class="bg-white/10 rounded-xl p-4 max-h-[108px] text-center"
          >
            <h6 class="font-bold text-lg sm:text-xl text-white mb-2 sm:mb-3">{{ item.title }}</h6>
            <p class="text-white text-sm sm:text-base">{{ item.description }}</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script lang="ts" setup>
import { aboutData } from '@/shared/aboutMock'
import type { AboutData } from '@/shared/types/about'

const about: AboutData = aboutData
</script>
