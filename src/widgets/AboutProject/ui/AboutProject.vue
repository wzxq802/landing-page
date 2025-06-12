<template>
    <section id="about" class="about bg-[url('/src/assets/images/about-project-bg.png')] bg-cover h-[486px] flex">
        <div class="container mx-auto flex items-center">
            <div class="max-w-3xl pl-24">
                <h2 class="font-bold text-4xl text-[#fff] mb-7">{{ about.title }}</h2>
                <p class="text-[#fff] mb-7"> {{ about.description }}</p>
                <div class="flex  gap-x-6">
                    <div v-for="(item, id) in about.items" :key="id" class="bg-white/10 rounded-xl p-3 w-64 max-h-[108px]">
                        <h6 class="font-bold text-xl text-[#fff] mb-3 text-center">{{ item.title }}</h6>
                        <p class="text-[#fff] text-center">{{ item.description }}</p>
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


