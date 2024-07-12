<template>
  <section>
    <div
      class="w-full px-[24px] mx-auto md:px-[48px] md:max-w-[calc(672px+48px+48px)] xl:max-w-[calc(1188px+48px+48px)]"
    >
      <div
        class="rounded-[16px] bg-gray-100 px-[24px] py-[48px] md:px-[48px] md:py-[64px] xl:py-[128px]"
      >
        <div class="mx-auto max-w-[836px]">
          <div
            class="w-full px-[24px] mx-auto md:px-[48px] md:max-w-[calc(672px+48px+48px)] xl:max-w-[calc(1188px+48px+48px)]"
          >
            <h1
              class="font-bold text-center text-gray-900 text-2xl md:text-3xl xl:text-4xl"
            >
              Wie viel wird von meiner Versicherung übernommen?
            </h1>
          </div>
          <div class="w-full h-[32px] md:h-[64px]"></div>
        
          <div class="relative">
            <button
              @click="showlist(), rotate()"
              class="relative flex px-[16px] border rounded-[8px] border-gray-300 bg-white py-[12px] w-full cursor-default"
            >
              <p class="w-full text-gray-900 text-left truncate text-base">
                <span v-if="selected === 0"> Versicherung wählen </span>
                <span v-if="selected === 1"> Axa </span>
                <span v-if="selected === 2"> CSS </span>
                <span v-if="selected === 3"> Helsana </span>
                <span v-if="selected === 4"> KPT </span>
                <span v-if="selected === 5"> Sanitas </span>
                <span v-if="selected === 6"> Swica </span>
                <span v-if="selected === 7"> Sympany </span>
                <span v-if="selected === 8"> Visana </span>
              </p>

              <div class="h-[24px] w-[24px] shrink-0">
                <img src="/assets/icon-chevron-down-gray.svg" alt="" />
              </div>
            </button>
            <ul
              v-show="show"
              class="p-[8px] border rounded-[8px] border-gray-300 bg-white text-left w-full absolute z-10 top-0"
            >
              <li
                @click="(selected = 1), showlist(), rotate()"
                :class="{
                  'bg-blue-600 text-white hover:bg-none}': selected === 1,
                  'hover:bg-gray-50': selected != 1,
                }"
                class="w-full px-[12px] py-[8px] rounded-[8px] cursor-default"
              >
                Axa
              </li>
              <li
                @click="(selected = 2), showlist(), rotate()"
                :class="{
                  'bg-blue-600 text-white }': selected === 2,
                  'hover:bg-gray-50': selected != 2,
                }"
                class="w-full p-[8px] rounded-[8px] cursor-default"
              >
                CSS
              </li>
              <li
                @click="(selected = 3), showlist(), rotate()"
                :class="{
                  'bg-blue-600 text-white }': selected === 3,
                  'hover:bg-gray-50': selected != 3,
                }"
                class="w-full p-[8px] rounded-[8px] cursor-default"
              >
                Helsana
              </li>
              <li
                @click="(selected = 4), showlist(), rotate()"
                :class="{
                  'bg-blue-600 text-white }': selected === 4,
                  'hover:bg-gray-50': selected != 4,
                }"
                class="w-full p-[8px] rounded-[8px] cursor-default"
              >
                KPT
              </li>
              <li
                @click="(selected = 5), showlist(), rotate()"
                :class="{
                  'bg-blue-600 text-white }': selected === 5,
                  'hover:bg-gray-50': selected != 5,
                }"
                class="w-full p-[8px] rounded-[8px] cursor-default"
              >
                Sanitas
              </li>
              <li
                @click="(selected = 6), showlist(), rotate()"
                :class="{
                  'bg-blue-600 text-white }': selected === 6,
                  'hover:bg-gray-50': selected != 6,
                }"
                class="w-full p-[8px] rounded-[8px] cursor-default"
              >
                Swica
              </li>
              <li
                @click="(selected = 7), showlist(), rotate()"
                :class="{
                  'bg-blue-600 text-white ': selected === 7,
                  'hover:bg-gray-50': selected != 7,
                }"
                class="w-full p-[8px] rounded-[8px] cursor-default"
              >
                Sympany
              </li>
              <li
                @click="(selected = 8), showlist(), rotate()"
                :class="{
                  'bg-blue-600 text-white ': selected === 8,
                  'hover:bg-gray-50': selected != 8,
                }"
                class="w-full p-[8px] rounded-[8px] cursor-default"
              >
                Visana
              </li>
            </ul>
            <div class="w-full h-[32px]"></div>
            <div
              class="grid grid-cols-1 gap-y-[16px] xl:grid-cols-2 xl:gap-y-[32px]"
            >
              <listText
                v-if="selected === 1"
                h3Msg="Gesundheit COMPLET"
                h4Msg="75% der Kosten bis max. CHF 1000.-"
                pMsg="alle 3 Jahre"
              ></listText>
              <listText
                v-if="selected === 1"
                h3Msg="Gesundheit ACTIF"
                h4Msg="75% der Kosten bis max. CHF 500.-"
                pMsg="alle 3 Jahre"
              ></listText>
              <listText
                v-if="selected === 2"
                h3Msg="myFlex (Premium)"
                h4Msg="50% bis CHF 500.-"
                pMsg="jedes Jahr"
              ></listText>
              <listText
                v-if="selected === 2"
                h3Msg="myFlex (Balance)"
                h4Msg="50% bis CHF 250.-"
                pMsg="jedes Jahr"
              ></listText>
              <listText
                v-if="selected === 2"
                h3Msg="myFlex (Economy)"
                h4Msg="50% bis CHF 150.-"
                pMsg="jedes Jahr"
              ></listText>
              <listText
                v-if="selected === 3"
                h3Msg="Sana"
                h4Msg="75% der Kosten bis max. CHF 500.-"
                pMsg="jedes Jahr"
              ></listText>
              <listText
                v-if="selected === 3"
                h3Msg="Completa (Plus)"
                h4Msg="90% der Kosten bis max. CHF 750.- (ergänzend nochmals 90% bis CHF 500.-)"
                pMsg="jedes Jahr"
              ></listText>
              <listText
                v-if="selected === 3"
                h3Msg="Primeo"
                h4Msg="Nein"
                pMsg="-"
              ></listText>
            </div>
            <div class="w-full h-[32px]"></div>
            <div
              class="w-full max-w-full text-left text-sm font-500 text-gray-500 md:text-center"
            >
              <p>
                Diese Liste umfasst die gängigsten Versicherungen, aber diese
                Details sind nur indikativ. Wir empfehlen, immer bei deiner
                individuellen Zusatzversicherung nachzusehen, um den genauen
                Beitrag zu erfahren.
              </p>
            </div>
            <div class="w-full h-[32px]"></div>
          </div>
        </div>
      </div>
    </div>
  </section>
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
