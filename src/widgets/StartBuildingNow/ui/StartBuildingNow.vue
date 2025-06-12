<template>
    <section id="start" class="start py-8 md:py-14">
        <div class="container mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex flex-col lg:flex-row justify-between items-center bg-[#EFF2F4] rounded-lg overflow-hidden">
                <div class="w-full lg:w-1/2 p-6 md:p-8 lg:p-12 xl:pl-14 order-2 lg:order-1">
                    <h2 class="font-bold text-2xl sm:text-3xl md:text-4xl text-[#000] mb-4 md:mb-7">
                        Готовы начать строительство своей мечты?
                    </h2>
                    <p class="text-base md:text-lg text-[#1E1E1E] mb-6">
                        Цифровая платформа, которая упрощает каждый этап — от идеи до эксплуатации.
                    </p>
                    <button class="w-full rounded-xl p-4 h-14 bg-[#00b359] text-[#fff] hover:bg-[#007439]" type="button">
                        Начать сейчас
                    </button>
                </div>
                <div class="w-full lg:w-1/2 order-1 lg:order-2">
                    <img 
                        src="@/assets/images/start_bg.png" 
                        alt="house" 
                        class="w-full h-auto object-cover lg:max-h-[400px] xl:max-h-none"
                    >
                </div>
            </div>
        </div>
    </section>
</template>

<script lang="ts" setup>
</script>