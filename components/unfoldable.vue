<template>
  <div class="rounded-[16px] bg-gray-50 p-[16px] md:p-[24px] xl:p-[32px]">
    <button
      class="flex gap-x-[24px] w-full"
      @click="
        unfold();
        shownav();
      "
    >
      <h3
        class="font-semibold text-base md:text-lg xl:text-xl grow text-start text-gray-900"
      >
        {{ h3 }}
      </h3>
      <div class="relative min-h-[24px] min-w-[24px]">
        <div
          class="absolute right-0 top-0 transition-transform "
          :class="{ 'rotate-90': rotate90 }"
        >
          <img src="/assets/icon-minus.svg" alt="" />
        </div>

        <div class="rotate-90">
          <img src="/assets/icon-minus.svg" alt="" />
        </div>
      </div>
    </button>

    <div v-if="show" class="overflow-hidden transition-all ease-in-out">
      <div class="w-full h-[12px] md:h-[24px]"></div>
      <div class="my-0 text-base font-500 xl:text-lg :underline text-gray-900">
        <p>
          {{ message }}
        </p>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";

defineProps({
  h3: String,
  message: String,
});
var show = ref(false);
var rotate90 = ref(false);
function shownav() {
  show.value = !show.value;
}
function unfold() {
  rotate90.value = !rotate90.value;
}
</script>
