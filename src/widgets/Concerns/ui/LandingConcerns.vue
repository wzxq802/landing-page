<template>
  <section class="py-16 bg-[#EFF2F4]">
    <div class="container mx-auto px-4 sm:px-6 lg:px-24 flex flex-col">
      <div class="grid grid-cols-1 sm:grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
        <div class="rounded-2xl overflow-hidden  relative group  flex flex-col" >
            <h2 class="font-bold text-4xl text-[#222] mb-7">Что волнует каждого застройщика?</h2>
        </div>
        <div v-for="item in concernsData" :key="item.id" class="rounded-2xl overflow-hidden relative group bg-white flex items-center justify-center flex-col py-4 px-8">
          <div class="a">
            <img :src="item.image" :alt="item.title" class="w-f16 h-16 group-hover:scale-105 transition-transform duration-300"/>
          </div>
          <div class="p-4 text-[#222] bg-transparent text-sm sm:text-base flex-grow flex items-end">
            {{ item.title }}
          </div>
        </div>
      </div>
    </div>
  </section>
</template>


<script lang="ts" setup>
import { concerns } from '@/shared/concernsMock';
import type { ConcernsData } from '@/shared/types/concerns'

const concernsData: ConcernsData[] = concerns
</script>
