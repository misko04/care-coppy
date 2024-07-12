<template>
  <div class="flex gap-[16px] md:flex-col md:items-center xl:gap-[24px]">
    <div class="flex justify-center">
      <img class="rounded-full" :src="`_nuxt/${img}.webp`" alt="" />
    </div>
    <div class="flex flex-col justify-center md:justify-start">
      <h3 class="text-lg font-bold xl:text-xl md:text-center">
        {{ h3Msg }}
      </h3>
      <p
        class="text-base font-semibold xl:text-lg md:text-center text-gray-400"
      >
        {{ pMsg }}
      </p>
    </div>
  </div>
</template>

<script setup>
defineProps({
  img: String,
  h3Msg: String,
  pMsg: String,
});
</script>
