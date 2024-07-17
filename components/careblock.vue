<template>
  <div>
    <div
      class="h-[48px] w-[48px] xl:h-[56px] xl:w-[56px] bg-primary-50 rounded-[16px] py-[12px] px-[12px] xl:py-[16px] xl:px-[16px]"
    >
      <div class="w-[24px] h-[24px]">
        <img :src="`_nuxt/assets/${img}`" class="w-full h-full" />
      </div>
    </div>

    <div>
      <div class="w-full h-0 md:h-[24px]"></div>
      <h3 class="text-lg font-bold xl:text-xl text-gray-900">
        {{ h3text }}
      </h3>
      <div class="w-full h-0 md:h-[8px]"></div>
      <p class="text-lg font-semibold text-gray-600">
        {{ ptext }}
      </p>
    </div>
  </div>
</template>

<script setup>

defineProps({
  h3text: String,
  ptext: String,
  img: String,
});
</script>
