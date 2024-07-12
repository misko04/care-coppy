<template>
  <a
    href=""
    class="rounded-[16px] border-2 border-gray-100 px-[24px] transition-all duration-300 hover:bg-gray-100 xl:px-[32px]"
    ><div class="w-full h-[24px]"></div>
    <h3 class="prose text-2xl font-semibold font-bold xl:text-3xl">
      <p>
        <b>{{ b }}</b>
        Check-up
      </p>
    </h3>
    <div class="w-full h-[16px]"></div>
    <p class="text-lg">
      {{ p }}
    </p>
    <div class="w-full h-[24px] md:h-[24px] xl:[32px]"></div>
  </a>
</template>

<script setup>
import { ref } from "vue";
var showvideo = ref(false);

defineProps({
  b: String,
  p: String,
});

function video() {
  showvideo.value = !showvideo.value;
}
</script>
