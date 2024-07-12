<template>
  <div class="border border-transparent rounded-[16px] cursor-pointer">
    <div class="flex gap-x-[16px] xl:gap-x-[24px]">
      <div
        class="bg-blue-50 w-[40px] h-[40px] rounded-full items-center justify-center flex shrink-0 font-semibold"
      >
        <p class="text-blue-500 text-lg font-bold">{{ num }}</p>
      </div>

      <div class="text-lg xl:text-xl text-left font-semibold">
        <h3 class="text-gray-900">
          {{ h3Msg }}
        </h3>
        <div class="w-full h-[8px]"></div>
        <p class="text-gray-500">{{ pMsg }}</p>
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
