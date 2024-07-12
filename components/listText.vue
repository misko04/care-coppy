<template>
  <div class="pb-[16px] xl:pb-[32px] border-b border-gray-300">
    <h3 class="font-bold">{{ h3Msg }}</h3>
    <h4>{{ h4Msg }}</h4>
    <p>{{ pMsg }}</p>
  </div>
</template>

<script setup>
defineProps({
  h3Msg: String,
  h4Msg: String,
  pMsg: String,
});
</script>
