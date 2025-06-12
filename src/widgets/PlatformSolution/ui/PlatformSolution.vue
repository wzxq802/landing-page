<template>
  <section id="" class="py-16">
    <div class="container flex justify-center flex-col mx-auto px-24">
      <h2 class="font-bold text-4xl text-[#222] mb-7">Решения платформы</h2>
      <div class="grid grid-cols-12 gap-4">
        <div v-for="item in platformData" :key="item.id" :class="['rounded-2xl overflow-hidden shadow-md relative group', item.id === 1 || item.id === 6 || item.id === 7 || item.id === 8 ? 'col-span-12 sm:col-span-6 md:col-span-6 lg:col-span-6' : 'col-span-6 sm:col-span-3 md:col-span-3 lg:col-span-3']">
          <img :src="item.image" :alt="item.title" class="w-full h-72 object-cover group-hover:scale-105 transition-transform duration-300`"/>
          <div class="absolute bottom-0 left-0 right-0 bg-gradient-to-t from-black/60 to-transparent bg-opacity-3 text-white p-4 text-sm sm:text-base">
            {{ item.title }}
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script lang="ts" setup>
import { solutions } from '@/shared/platformSolutionMock';
import type { SolutionData } from '@/shared/types/platform'

const platformData: SolutionData[] = solutions
</script>
