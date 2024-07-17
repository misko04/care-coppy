<template>
  <div
    class="grid md:grid-cols-2 md:gap-x-[48px] xl:gap-x-[72px] items-center"
    v-editable="blok"
  >
    <div :class="`md:col-span-1 ${order}`">
      <img
        class="w-full h-full object-cover rounded-[16px] xl:rounded-[24px]"
        :src="`_nuxt/assets/${blok.img}`"
        alt=""
      />
    </div>
    <div class="md:order-1 md:col-span-1">
      <h3 class="text-xl xl:text-3xl md:text-2xl font-bold">
        {{ blok.h3text }}
      </h3>
      <div class="w-full h-[12px] md:h-[16px]"></div>
      <div class="text-base xl:text-xl text-gray-500 font-medium">
        <p>
          {{ blok.ptext }}
        </p>
      </div>
    </div>
  </div>
</template>

<script setup>
defineProps({
  order: String,
  blok: { img: String, h3text: String, ptext: String },
});
</script>
