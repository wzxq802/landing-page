<template>
  <footer class="bg-[#222222] text-white py-8 px-4 sm:px-6 lg:px-8">
    <div class="container mx-auto">
      <div class="pl-0 sm:pl-8">
        <h2 class="text-2xl font-bold mb-4">2STORYHOUSE</h2>
      </div>
      <div class="grid grid-cols-1 gap-8 mb-8 px-0 sm:px-8">
        <div class="flex flex-col gap-4 sm:flex-row sm:flex-wrap sm:justify-between">
          <p class="flex items-center">
            <PhoneIcon class="h-5 w-5 mr-2" />
            +7 (000) 000-00-00
          </p>
          <a href="mailto:2storyhouse@yandex.ru" class="flex items-center">
            <EnvelopeIcon class="h-5 w-5 mr-2" />
            2storyhouse@yandex.ru
          </a>
          <p class="flex items-start">
            <MapPinIcon class="h-5 w-5 mr-2 mt-1 flex-shrink-0" />
            Санкт-Петербург. улица Невского, офис 0
          </p>
          <a href="https://www.psd.ru/" class="flex items-center">
            <ClockIcon class="h-5 w-5 mr-2" />
            Режим работы: 9:00-18:00
          </a>
        </div>
        <ul class="flex flex-wrap gap-x-4 gap-y-2">
          <li><a href="#">О проекте</a></li>
          <li><a href="#">Наша платформа</a></li>
          <li><a href="#">Решения платформы</a></li>
          <li><a href="#">Преимущества</a></li>
          <li><a href="#">Как работает</a></li>
          <li><a href="#">Аудитория</a></li>
          <li><a href="#">Контакты</a></li>
        </ul>
        <ul class="flex flex-wrap gap-x-4 gap-y-2">
          <li><a class="text-[#9B9B9B]" href="#">Условия использования</a></li>
          <li><a class="text-[#9B9B9B]" href="#">Политика конфиденциальности</a></li>
          <li><a class="text-[#9B9B9B]" href="#">Поддержка</a></li>
        </ul>
      </div>
      <div class="pt-6 px-0 sm:px-8">
        <p class="text-white mb-2 md:mb-0">© 2025</p>
        <p class="text-white">Все права защищены</p>
      </div>
    </div>
  </footer>
</template>

<script setup lang="ts">
import { PhoneIcon, EnvelopeIcon, MapPinIcon, ClockIcon } from '@heroicons/vue/24/outline';
</script>
