<template>
  <div class="border border-transparent rounded-[16px] cursor-pointer">
    <div class="flex gap-[16px] xl:flex-col xl:gap-[24px]">
      <div
        class="bg-gray-50 w-[32px] h-[32px] rounded-full items-center justify-center flex shrink-0 font-semibold"
      >
        <p class="text-lg font-bold">{{ num }}</p>
      </div>

      <div class="text-lg xl:text-xl text-left font-semibold">
        <h3 class="text-gray-900">
          {{ h3Msg }}
        </h3>
        <div class="w-full h-[8px]"></div>
        <p class="text-gray-500 text-base font-medium">{{ pMsg }}</p>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";

defineProps({
  num: String,
  h3Msg: String,
  pMsg: String,
});
</script>
