<template>
  <button class="relative h-full w-full" @click="video()">
    <picture class="overflow-hidden">
      <img
        :src="`_nuxt/assets/${img}`"
        class="h-full w-full object-cover object-right"
      />
    </picture>
  </button>
  <div class="z-[10] w-[100px] h-[100px]" v-show="showvideo">aa</div>
</template>

<script setup>
import { ref } from "vue";  
var showvideo = ref(false);
defineProps({
  img: String,
});

function video() {
  showvideo = !showvideo;
}
</script>
