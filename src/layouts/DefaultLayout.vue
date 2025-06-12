<template>
  <div>
    <LandingHeader/>
    <LandingHero/>
    <AboutProject/>
    <PlatformSolution/>
    <Concerns/>
    <SwiperSlider/>
  </div>
</template>

<script setup lang="ts">
import LandingHeader from '@/widgets/LandingHeader/ui/LandingHeader.vue'
import LandingHero from '@/widgets/LandingHero/ui/LandingHero.vue'
import AboutProject from '@/widgets/AboutProject/ui/AboutProject.vue'
import PlatformSolution from '@/widgets/PlatformSolution/ui/PlatformSolution.vue'
import Concerns from '@/widgets/Concerns/ui/LandingConcerns.vue'
import SwiperSlider from '@/widgets/SwiperSlider/ui/SwiperSlider.vue'
</script>
