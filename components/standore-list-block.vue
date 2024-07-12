<template>
  <div
    class="w-full px-[24px] mx-auto md:px-[48px] md:max-w-[calc(672px+48px+48px)] xl:max-w-[calc(1188px+48px+48px)]"
  >
    <div></div>
    <div
      class="bg-gray-100 xl:py-[128px] rounded-[16px] px-[24px] py-[48px] md:px-[48px] md:py-[64px]"
    >
      <h3 class="text-center font-bold text-2xl md:text-3xl xl:text-4xl">
        Bald auch in deiner Stadt
      </h3>
      <div class="w-full h-[12px]"></div>
      <p class="text-center text-base xl:text-lg">
        Werde benachrichtigt sobald weiter CARE Stores verfügbar sind
      </p>
      <div class="w-full h-[32px]"></div>
      <div
        class="grid grid-cols-1 gap-[16px] xl:mx-auto xl:w-min xl:grid-cols-[284px,284px,min-content]"
      >
        <div class="relative">
          <button
            @click="showlist(), rotate()"
            class="relative flex px-[16px] border rounded-[8px] border-gray-300 bg-white py-[12px] w-full cursor-default"
          >
            <p class="w-full text-gray-900 text-left truncate text-base">
              <span v-if="selected === 0"> Versicherung wählen </span>
              <span v-if="selected === 1"> Aarau </span>
              <span v-if="selected === 2"> Baden </span>
              <span v-if="selected === 3"> Bellinzona </span>
              <span v-if="selected === 4"> Biel </span>
              <span v-if="selected === 5"> Chur </span>
              <span v-if="selected === 6"> Freiburg </span>
              <span v-if="selected === 7"> Genf </span>
              <span v-if="selected === 8"> Liestal </span>
              <span v-if="selected === 9"> Lugano </span>
              <span v-if="selected === 10"> Montreux </span>
              <span v-if="selected === 11"> Morges </span>
              <span v-if="selected === 12"> Neuchâtel </span>
            </p>

            <div class="h-[24px] w-[24px] shrink-0">
              <img src="/assets/icon-chevron-down-gray.svg" alt="" />
            </div>
          </button>
          <ul
            v-show="show"
            class="absolute top-0 max-h-[376px] w-full overflow-auto rounded-[8px] border border-gray-300 bg-white p-[8px] shadow-xl focus:outline-none"
          >
            <li
              @click="(selected = 1), showlist(), rotate()"
              :class="{
                'bg-blue-600 text-white hover:bg-none}': selected === 1,
                'hover:bg-gray-50': selected != 1,
              }"
              class="w-full px-[12px] py-[8px] rounded-[8px] cursor-default"
            >
              Aarau
            </li>
            <li
              @click="(selected = 2), showlist(), rotate()"
              :class="{
                'bg-blue-600 text-white }': selected === 2,
                'hover:bg-gray-50': selected != 2,
              }"
              class="w-full p-[8px] rounded-[8px] cursor-default"
            >
              Baden
            </li>
            <li
              @click="(selected = 3), showlist(), rotate()"
              :class="{
                'bg-blue-600 text-white }': selected === 3,
                'hover:bg-gray-50': selected != 3,
              }"
              class="w-full p-[8px] rounded-[8px] cursor-default"
            >
              Bellinzona
            </li>
            <li
              @click="(selected = 4), showlist(), rotate()"
              :class="{
                'bg-blue-600 text-white }': selected === 4,
                'hover:bg-gray-50': selected != 4,
              }"
              class="w-full p-[8px] rounded-[8px] cursor-default"
            >
              Biel
            </li>
            <li
              @click="(selected = 5), showlist(), rotate()"
              :class="{
                'bg-blue-600 text-white }': selected === 5,
                'hover:bg-gray-50': selected != 5,
              }"
              class="w-full p-[8px] rounded-[8px] cursor-default"
            >
              Chur
            </li>
            <li
              @click="(selected = 6), showlist(), rotate()"
              :class="{
                'bg-blue-600 text-white }': selected === 6,
                'hover:bg-gray-50': selected != 6,
              }"
              class="w-full p-[8px] rounded-[8px] cursor-default"
            >
              Freiburg
            </li>
            <li
              @click="(selected = 7), showlist(), rotate()"
              :class="{
                'bg-blue-600 text-white ': selected === 7,
                'hover:bg-gray-50': selected != 7,
              }"
              class="w-full p-[8px] rounded-[8px] cursor-default"
            >
              Genf
            </li>
            <li
              @click="(selected = 8), showlist(), rotate()"
              :class="{
                'bg-blue-600 text-white ': selected === 8,
                'hover:bg-gray-50': selected != 8,
              }"
              class="w-full p-[8px] rounded-[8px] cursor-default"
            >
              Liestal
            </li>
            <li
              @click="(selected = 9), showlist(), rotate()"
              :class="{
                'bg-blue-600 text-white ': selected === 9,
                'hover:bg-gray-50': selected != 9,
              }"
              class="w-full p-[8px] rounded-[8px] cursor-default"
            >
              Lugano
            </li>
            <li
              @click="(selected = 10), showlist(), rotate()"
              :class="{
                'bg-blue-600 text-white ': selected === 10,
                'hover:bg-gray-50': selected != 10,
              }"
              class="w-full p-[8px] rounded-[8px] cursor-default"
            >
              Montreux
            </li>
            <li
              @click="(selected = 11), showlist(), rotate()"
              :class="{
                'bg-blue-600 text-white ': selected === 11,
                'hover:bg-gray-50': selected != 11,
              }"
              class="w-full p-[8px] rounded-[8px] cursor-default"
            >
              Morges
            </li>
            <li
              @click="(selected = 12), showlist(), rotate()"
              :class="{
                'bg-blue-600 text-white ': selected === 12,
                'hover:bg-gray-50': selected != 12,
              }"
              class="w-full p-[8px] rounded-[8px] cursor-default"
            >
              Neuchâtel
            </li>
          </ul>
        </div>
        <div>
          <input
            class="relative flex w-full items-center justify-between gap-x-[10px] rounded-[8px] border border-gray-300 bg-white px-[16px] py-[12px] focus:outline-none"
            type="email"
            placeholder="Email Adresse"
          />
        </div>
        <button
          class="bg-blue-600 rounded-full text-white px-[23px] py-[11px] text-base"
        >
          Abschicken
        </button>
      </div>
    </div>
  </div>
</template>


<script setup>
var show = ref(false);
var showArrow = ref(false);
var selected = 0;
function showlist() {
  show.value = !show.value;
}
function rotate() {
  showArrow.value = !showArrow.value;
}
</script>
