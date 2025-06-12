<template>
  <section class="work bg-[#EFF2F4] py-12">
    <div class="container mx-auto px-4 md:px-6">
      <h2 class="px-14 font-bold text-3xl md:text-4xl text-[#222] mb-7 text-center md:text-left">Как работает платформа</h2>
      <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-5 gap-6">
        <div v-for="item in howWorkData" :key="item.id" class="bg-white p-4 rounded-lg hover:shadow-lg transition-shadow h-full">
          <div class="flex items-center h-full">
            <div class="bg-[#00B359] text-white rounded-full w-8 h-8 flex-shrink-0 flex items-center justify-center mr-3">
              <span class="leading-none block transform translate-y-[1px]">{{ item.id }}</span>
            </div>
            <h3 class="text-md leading-tight align-middle">
              {{ item.title }}
            </h3>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script lang="ts" setup>
import { howWork } from '@/shared/howWorkMock'
import type { HowWorkData } from '@/shared/types/howWork'

const howWorkData: HowWorkData[] = howWork
</script>