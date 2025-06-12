<template>
  <div>
    <LandingHeader/>
    <LandingHero/>
    <AboutProject/>
    <PlatformSolution/>
    <Concerns/>
  </div>
</template>

<script setup lang="ts">
import LandingHeader from '@/widgets/LandingHeader/ui/LandingHeader.vue'
import LandingHero from '@/widgets/LandingHero/ui/LandingHero.vue'
import AboutProject from '@/widgets/AboutProject/ui/AboutProject.vue'
import PlatformSolution from '@/widgets/PlatformSolution/ui/PlatformSolution.vue'
import Concerns from '@/widgets/Concerns/ui/Concerns.vue'
</script>
