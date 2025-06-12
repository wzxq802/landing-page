<template>
  <section class="advantages py-10 bg-[linear-gradient(to_right,rgba(0,0,0,0.9),transparent),url('/src/assets/images/target_bg.png')] bg-cover h-[486px] md:py-14 my-10 md:my-28 relative">
    <div class="container mx-auto px-4 md:px-6">
      <div class="flex flex-col px-14 lg:flex-row gap-8 lg:gap-12 xl:gap-16">
        <div class="lg:order-2">
          <h2 class="font-bold text-2xl sm:text-3xl md:text-4xl text-white mb-5 md:mb-7">
            Целевая аудитория
          </h2>
          <ul class="space-y-3 md:space-y-4">
            <li 
              v-for="item in targetData" 
              :key="item.id" 
              class="flex items-start gap-3 md:gap-4 text-white"
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
import { target } from '@/shared/targetMock'
import type { TargetData } from '@/shared/types/target'
const targetData: TargetData[] = target
</script>