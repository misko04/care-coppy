<template>
  <div
    class="flex flex-col justify-between gap-[32px] rounded-[16px] border border-gray-200 p-[24px] md:flex-row xl:flex-col"
  >
    <div class="flex flex-col gap-[16px] md:w-1/2 xl:w-auto">
      <p class="font-bold text-2xl">{{ city }}</p>
      <p
        class="w-fit rounded-[16px] bg-blue-50 px-[8px] py-[4px] text-xs font-700 text-blue-600"
        :class="`${hiden}`"
      >
        Flagship Store
      </p>
      <p class="text-base font-medium xl:text-lg text-gray-900">{{ ptext }}</p>
      <p class="text-base font-semibold xl:text-lg text-gray-900">
        {{ address }}
      </p>
      <div class="text-base xl:text-lg font-medium text-gray-500">
        <p>{{ openh }}</p>
        <p class="underline">{{ mail }}</p>
        <p class="underline">{{ phone }}</p>
      </div>
    </div>
    <div class="flex flex-col gap-[16px] md:w-1/2 md:justify-center xl:w-auto">
      <div class="justify-start gap-[18px] md:gap-[24px] w-full">
        <a
          class="block cursor-pointer rounded-full text-center relative bg-blue-600 py-[11px] px-[25px] text-white w-full"
          >Check-up buchen</a
        >
      </div>
      <div class="justify-start gap-[18px] md:gap-[24px] w-full">
        <a
          class="block cursor-pointer rounded-full text-center relative bg-gray-100 py-[11px] px-[25px] text-black w-full"
          >Route</a
        >
      </div>
    </div>
  </div>
</template>

<script setup>
defineProps({
  city: String,
  address: String,
  openh: String,
  phone: String,
  mail: String,
  hiden: String,
  ptext: String,
});
</script>
