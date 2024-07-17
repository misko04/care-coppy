<template>
  <head>
    <link href="https://fonts.cdnfonts.com/css/noah" rel="stylesheet" />
  </head>
  <section class="bg-a mt-[-64px] xl:mt-[-128px] bg-blue-700">
    <div class="relative overflow-hidden" v-editable="block">
      <div class="w-full h-[130px] xl:h-[256px]"></div>
      <div
        class="w-full px-[24px] mx-auto md:px-[48px] md:max-w-[calc(672px+48px+48px)] xl:max-w-[calc(1188px+48px+48px)]"
      >
        <div class="xl:relative">
          <div class="relative z-[20] xl:max-w-[592px]">
            <h1
              class="text-4xl font-semibold text-white md:text-[40px] xl:text-6xl xl:leading-[110%] font-sans"
            >
              Optimiere deine Gesundheit
            </h1>
            <div class="w-full h-[32px]"></div>
            <h3 class="text-2xl font-bold text-white">
              Der modernste Check-up der Schweiz, komplett digital und mit
              ärztlicher Begleitung.
            </h3>
            <div class="w-full h-[32px]"></div>
            <div
              class="flex items-center justify-start gap-[18px] md:gap-[24px]"
            >
              <a
                class="block max-w-max rounded-full text-center relative border bg-white border-white py-[11px] px-[25px]"
                >Check-up buchen</a
              >
            </div>
            <div class="w-full h-[250px] md:h-[32px] xl:h-[152px]"></div>
            <div
              class="flex flex-col gap-x-[32px] gap-y-[12px] md:flex-row md:justify-center xl:justify-start text-center items-center"
            >
              <div class="flex space-x-[10px]">
                <div class="h-[24px] w-[24px] flex">
                  <img src="../assets/google.svg" class="h-full w-full" />
                </div>
                <div class="flex justify-center text-center items-center">
                  <div class="flex space-x-[2px]">
                    <star />
                    <star />
                    <star />
                    <star />
                    <star />
                  </div>
                  <p
                    class="text-white text-lg pl-[10px] text-center justify-center underline underline-offset-[4px]"
                  >
                    4.8
                  </p>
                </div>
              </div>

              <div class="flex space-x-[10px]">
                <div class="h-[25px] w-[25px]">
                  <img
                    src="../assets/icon-checkmark-square-white.svg"
                    class="h-full w-full"
                  />
                </div>
                <div class="items-center">
                  <p class="text-white text-sm font-medium">
                    Anerkannt von Zusatzversicherungen
                  </p>
                </div>
              </div>
            </div>
            <div class="w-full h-[24px] md:h-[24px] xl:h-[70px]"></div>
          </div>

          <div
            class="absolute bottom-0 left-[calc(50%+40px)] z-[10] h-[326px] w-[444px] translate-x-[-50%] md:left-[50%] md:h-[334px] md:w-[768px] xl:left-auto xl:right-[-240px] xl:h-[720px] xl:w-[1000px] xl:translate-x-0"
          >
            <picture>
              <img src="../assets/homepage.png" />
            </picture>
          </div>
        </div>
      </div>
    </div>
  </section>
  <div class="w-full h-[150px] md:h-[95px] xl:h[120px]"></div>

  <section>
    <div
      class="w-full px-[24px] mx-auto md:px-[48px] md:max-w-[calc(672px+48px+48px)] xl:max-w-[calc(1188px+48px+48px)]"
    >
      <div
        class="grid grid-cols-1 gap-y-[40px] md:grid-cols-2 md:gap-x-[16px] xl:gap-x-[32px]"
      >
        <div>
          <h3 class="text-4xl font-bold">
            Umfangreiche und einfach zugängliche Gesundheitschecks
          </h3>
          <div class="w-full h-[16px] xl:h-[24px]"></div>
          <div class="w-full h-[32px] xl:h-[48px]"></div>
          <div class="flex items-center justify-start gap-[18px] md:gap-[24px]">
            <a
              class="block max-w-max rounded-full text-center relative border bg-blue-600 border-white py-[11px] px-[25px] text-white"
              >Check-up buchen</a
            >
          </div>
        </div>

        <div class="flex flex-col gap-y-[24px]">
          <checkupBlock
            b="Blut"
            p="Analyse wichtiger Biomarker in deinem Blut für wertvolle Einblicke in deinen Gesundheitszustand."
          />
          <checkupBlock
            b="Ganzkörper"
            p="Umfassende Analyse deines gesamten Körpers für einen tiefen Einblick in deine Gesundheit."
          />
        </div>
      </div>
    </div>
  </section>
  <div class="w-full h-[32px] md:h-[48px] xl:h-[96px]"></div>
  <section>
    <div
      class="w-full px-[24px] mx-auto md:px-[48px] md:max-w-[calc(672px+48px+48px)] xl:max-w-[calc(1370px+48px+48px)] hidden xl:block"
    >
      <div
        class="gap-x-[24px] gap-y-[32px] md:gap-y-[48px] xl:gap-x-[32px] md:grid-cols-2 xl:grid-cols-2 grid-cols-1 grid"
      >
        <div
          style="
            display: flex;
            flex-basis: 400px;
            gap: 32px;
            flex-direction: column;
            flex-grow: 1;
            min-width: 0;
          "
        >
          <div
            class="relative overflow-hidden bg-gray-100 px-0 xl:rounded-[16px] xl:px-[64px]"
          >
            <div
              class="w-full xl:w-full xl:px-0 px-[24px] mx-auto md:px-[48px] md:max-w-[calc(672px+48px+48px)] xl:max-w-[calc(916px+48px+48px)]"
            >
              <div class="w-full h-[64px]"></div>
              <h2 class="text-center text-4xl font-bold">
                Erhalte personalisierte Empfehlungen
              </h2>
              <div class="w-full h-[12px]"></div>
              <p class="text-center text-lg text-gray-500 font-semibold">
                Unsere Fachärzte und Health Coaches begleiten dich auf deinem
                Weg zu einem längeren und gesünderen Leben.
              </p>
              <div class="w-full h-[24px]"></div>
              <div class="flex flex-col items-center">
                <img src="/assets/people.webp" alt="" />
              </div>
            </div>
          </div>

          <div
            class="relative overflow-hidden bg-gray-100 px-0 py-[64px] xl:rounded-[16px] xl:p-[64px]"
          >
            <div
              class="w-full xl:w-full xl:px-0 px-[24px] mx-auto md:px-[48px] md:max-w-[calc(672px+48px+48px)] xl:max-w-[calc(916px+48px+48px)]"
            >
              <h2 class="text-center text-4xl font-bold">
                Von deiner Zusatzversicherung abgedeckt
              </h2>
              <div class="w-full h-[12px]"></div>
              <p class="text-center text-lg text-gray-500 font-semibold">
                Unsere Dienstleistungen werden von den meisten
                Zusatzversicherungen in der Schweiz rückvergütet. Erfahre, wie
                du eine Rückerstattung erhalten kannst.
              </p>
              <div class="w-full h-[24px]"></div>
              <div class="flex flex-col items-center">
                <img src="/assets/sponsors.webp" alt="" />
              </div>
              <div class="w-full h-[24px]"></div>
              <div class="flex justify-center">
                <a
                  class="block max-w-max rounded-full text-center relative border bg-gray-900 border-white py-[11px] px-[25px] text-white"
                  >Mehr erfahren</a
                >
              </div>
            </div>
          </div>
        </div>
        <div
          style="
            display: flex;
            flex-basis: 400px;
            flex-direction: column;
            flex-grow: 1;
            gap: 32px;
            min-width: 0;
          "
        >
          <div>
            <div class="w-full h-[80px]"></div>
            <div
              class="relative overflow-hidden bg-gray-100 px-0 xl:rounded-[16px] xl:px-[64px]"
            >
              <div
                class="w-full xl:w-full xl:px-0 px-[24px] mx-auto md:px-[48px] md:max-w-[calc(672px+48px+48px)] xl:max-w-[calc(916px+48px+48px)]"
              >
                <div class="w-full h-[64px]"></div>
                <h2 class="text-center text-4xl font-bold">
                  Tracke deine Gesundheit komplett digital
                </h2>
                <div class="w-full h-[12px]"></div>
                <p class="text-center text-lg text-gray-500 font-semibold">
                  Verfolge deinen Gesundheitszustand und erfahre mehr über die
                  wichtigsten Werte. Erhalte KI-gestützte Ratschläge von deinem
                  persönlichen virtuellen Coach.
                </p>
                <div class="w-full h-[24px]"></div>
                <div class="flex flex-col items-center">
                  <img src="/assets/phone.webp" alt="" />
                </div>
              </div>
            </div>
          </div>

          <div
            class="relative overflow-hidden bg-gray-100 px-0 py-[64px] xl:rounded-[16px] xl:p-[64px]"
          >
            <div
              class="w-full xl:w-full xl:px-0 px-[24px] mx-auto md:px-[48px] md:max-w-[calc(672px+48px+48px)] xl:max-w-[calc(916px+48px+48px)]"
            >
              <h2 class="text-center text-4xl font-bold">Weitere Services</h2>
              <div class="w-full h-[12px]"></div>
              <p class="text-center text-lg text-gray-500 font-semibold">
                Neben deinem Check-up kannst du deine Gesundheit mit
                zusätzlichen Blutanalysen, kardio-respiratorischen Tests,
                Coachings oder Supplements verbessern.
              </p>
              <div class="w-full h-[24px]"></div>
              <div class="flex flex-col items-center">
                <img src="/assets/services.webp" alt="" />
              </div>
              <div class="w-full h-[24px]"></div>
              <div class="flex justify-center">
                <a
                  class="block max-w-max rounded-full text-center relative border bg-black border-white py-[11px] px-[25px] text-white"
                  >Alle Services</a
                >
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
  <div class="w-full h-[32px] md:h-[48px] xl:h-[128px]"></div>
  <section class="bg-black">
    <div
      class="w-full px-[24px] mx-auto md:px-[48px] md:max-w-[calc(672px+48px+48px)] xl:max-w-[calc(1188px+48px+48px)]"
    >
      <div class="w-full h-[32px] md:h-[64px] xl:h-[96px]"></div>
      <div class="flex flex-col items-center text-center">
        <h1
          class="font-bold text-3xl max-w-[545px] text-white xl:max-w-[842px] xl:text-5xl text-center"
        >
          Warum ist es so schwer, gesund zu bleiben?
        </h1>
        <div class="h-[12px]"></div>
        <p
          class="my-0 font-semibold xl:text-lg text-gray-400 mx-auto text-center text-lg md:text-base xl:max-w-[622px] max-w-[545px] prose-p:text-lg md:prose-p:text-base"
        >
          Im hektischen Alltag ist es fast unmöglich, gesunde Gewohnheiten zu
          entwickeln. Der begrenzte Zugang zu moderner Diagnostik und den
          persönlichen Gesundheitsdaten erschwert dies zusätzlich.
        </p>
      </div>
      <div class="w-full h-[32px] md:h-[64px] xl:h-[96px]"></div>
    </div>
  </section>

  <div class="w-full h-[32px] md:h-[64px] xl:h-[96px]"></div>
  <section>
    <h2
      class="font-bold text-center text-gray-900 text-2xl md:text-3xl xl:text-4xl"
    >
      Wie CARE dir dabei hilft
    </h2>
    <div class="w-full h-[24px] md:h-[32px] xl:h-[48px]"></div>

    <div
      class="w-full px-[24px] mx-auto md:px-[48px] md:max-w-[calc(672px+48px+48px)] xl:max-w-[calc(1188px+48px+48px)]"
    >
      <div
        class="gap-x-[24px] gap-y-[32px] md:gap-y-[48px] xl:gap-x-[32px] md:grid-cols-2 xl:grid-cols-3 grid-cols-1 grid"
      >
        <careblock
          h3text="Überwache wichtige Gesundheitswerte"
          ptext="Behalte deine Gesundheit im Auge und beobachte, wie sich deine Werte im Laufe der Zeit verändern."
          img="icon-dashboard-blue.svg"
        />
        <careblock
          h3text="Erhalte personalisierte Ratschläge"
          ptext="Erhalte massgeschneiderte Empfehlungen in den Bereichen Ernährung, Bewegung, Schlaf und Stressmanagement."
          img="icon-dumbell-blue.svg"
        />
        <careblock
          h3text="Nutze moderne Diagnostik"
          ptext="Dank modernen Diagnosetechnologien erkennst du mögliche Krankheiten frühzeitig und kannst entsprechend handeln."
          img="icon-droplet-blue.svg"
        />
        <careblock
          h3text="Sprich mit erfahrenen Ärzten"
          ptext="Unsere Fachärzte und Experten beraten dich ganzheitlich im Bereich Präventivmedizin."
          img="icon-users-blue.svg"
        />
        <careblock
          h3text="Digitaler Zugang zu Gesundheitsdaten"
          ptext="Greife jederzeit auf deine Gesundheitsdaten zu und verfolge den Fortschritt über unsere benutzerfreundliche App."
          img="icon-smartphone-blue.svg"
        />
        <careblock
          h3text="Spare Kosten auf lange Sicht"
          ptext="Durch die Vermeidung von chronischen Krankheiten kannst du langfristig Kosten sparen und das System entlasten."
          img="icon-wallet-blue.svg"
        />
      </div>
    </div>
  </section>

  <div class="w-full h-[32px] md:h-[64px] xl:h-[96px]"></div>
  <section class="bg-gray-50">
    <div class="w-full h-[32px] md:h-[64px] xl:h-[96px]"></div>
    <div
      class="w-full px-[24px] mx-auto md:px-[48px] md:max-w-[calc(672px+48px+48px)] xl:max-w-[calc(1188px+48px+48px)]"
    >
      <h3 class="text-center text-4xl font-bold">Was unsere Kunden sagen</h3>
      <div class="w-full h-[24px] md:h-[32px] xl:h-[48px]"></div>
      <div class="flex gap-x-[32px]">
        <div
          @mouseover="shhower1"
          :class="{ 'xl:aspect-[1240/806] xl:flex-[2.2]': hower1 }"
          class="h-[607px] overflow-hidden rounded-[16px] md:h-[403px] w-fit flex-1 shrink transition-all duration-300"
        >
          <slider img="filters_format1.webp" class="w-full h-full" />
        </div>

        <div
          @mouseover="shhower2"
          :class="{ 'xl:aspect-[1240/806] xl:flex-[2.2]': hower2 }"
          class="h-[607px] overflow-hidden rounded-[16px] md:h-[403px] w-fit flex-1 shrink grow transition-all duration-300"
        >
          <slider img="filters_format2.webp" class="w-full h-full" />
        </div>
        <div
          @mouseover="shhower3"
          :class="{ 'xl:aspect-[1240/806] xl:flex-[2.2]': hower3 }"
          class="h-[607px] overflow-hidden rounded-[16px] md:h-[403px] w-fit flex-1 shrink grow transition-all duration-300"
        >
          <slider img="filters_format.webp" class="w-full h-full" />
        </div>
      </div>
      <div class="w-full h-[24px] md:h-[32px] xl:h-[96px]"></div>
    </div>
  </section>
  <section>
    <div class="w-full h-[32px] md:h-[48px] xl:h-[96px]"></div>
    <div
      class="w-full px-[24px] mx-auto md:px-[48px] md:max-w-[calc(672px+48px+48px)] xl:max-w-[calc(1188px+48px+48px)]"
    >
      <div class="grid grid-cols-1 xl:grid-cols-12">
        <div
          class="space-y-[32px] md:space-y-[48px] xl:col-start-3 xl:col-end-11 xl:space-y-[64px]"
        >
          <h1 class="text-2xl font-bold md:text-3xl xl:text-4xl text-gray-900">
            Häufige Fragen
          </h1>
          <ul class="space-y-[16px]">
            <li>
              <unfoldable
                h3="Werde ich von medizinischem Fachpersonal betreut?"
                message="Die Laboranalysen und Behandlungen werden von in der Schweiz zertifizierten medizinischem Fachpersonal durchgeführt, darunter Fachärzt:innen und medizinische Praxisassistent:innen. Alle nicht-klinischen Gesundheitsberatungsleistungen werden von unseren Health Coaches erbracht."
              />
            </li>
            <li>
              <unfoldable
                class="transition-all ease-in-out duration-300"
                h3="Wer gehört zum Ärzt:innenteam?"
                message="Unser Ärzt:innenteam besteht aus hochqualifizierten Fachärzt:innen aus der Schweiz. Eine Übersicht unserer erfahrenen Ärzt:innen findest du auf der Seite “Über CARE”."
              />
            </li>
            <li>
              <unfoldable
                h3="Sind die bei CARE angebotenen Lösungen sicher?"
                message="Natürlich; Sicherheit ist unsere oberste Priorität! Alle unsere Ärzt:innen und medizinischen Praxisassistent:innen sind in der Schweiz akkreditiert und unsere Standorte entsprechen allen lokalen Vorschriften. Darüber hinaus stehen Ihnen unsere Health Coaches zur Verfügung, um einen ganzheitlichen und umfassenden Ansatz anzubieten."
              />
            </li>
            <li>
              <unfoldable
                h3="Sind unsere Services evidenzbasiert?"
                message="Auf jeden Fall! Unsere Services sind evidenzbasiert und auf deine langfristige, nachhaltige Gesundheit ausgerichtet. Gemeinsam legen wir mit bewährten klinischen Methoden und wissenschaftlichen Erkenntnissen den Grundstein für ein gesünderes und erfüllteres Leben."
              />
            </li>
          </ul>
        </div>
      </div>
    </div>
  </section>
  <div class="w-full h-[32px] md:h-[48px] xl:h-[96px]"></div>
  <section>
    <div
      class="w-full px-[24px] mx-auto md:px-[48px] md:max-w-[calc(672px+48px+48px)] xl:max-w-[calc(1188px+48px+48px)] relative"
    >
      <div
        class="bg-blue-600 relative isolate mx-auto min-h-[513px] overflow-hidden rounded-[24px] px-[24px] py-[32px] md:grid md:min-h-[268px] md:grid-cols-2 md:gap-x-[24px] md:px-[48px] xl:min-h-[512px] xl:max-w-none xl:px-[108px]"
      >
        <div class="flex flex-col items-center justify-center md:items-start">
          <h3 class="text-white text-4xl">
            Beginne heute deine Gesundheit besser zu verstehen
          </h3>
          <div class="w-full h-[32px] md:h-[24px] xl:h-[32px]"></div>
          <div
            class="flex flex-cols items-center justify-start gap-[18px] md:gap-[24px]"
          >
            <a
              class="block max-w-max rounded-full text-center relative border bg-white border-white py-[11px] px-[25px]"
              >Check-up buchen</a
            >
          </div>
        </div>
        <div class="flex md:flex md:w-full md:items-center md:justify-end">
          <img src="/assets/eye.webp" alt="" />
        </div>
      </div>
    </div>
  </section>
  <div class="w-full h-[32px] md:h-[48px] xl:h-[96px]"></div>
</template>

<script setup>
defineProps<{
  block:{

  }
}>()
var hower1 = ref(true);
var hower2 = ref(false);
var hower3 = ref(false);

function shhower1() {
  hower1.value = true;
  hower2.value = false;
  hower3.value = false;
}
function shhower2() {
  hower1.value = false;
  hower2.value = true;
  hower3.value = false;
}
function shhower3() {
  hower1.value = false;
  hower2.value = false;
  hower3.value = true;
}
</script>

<style>
body {
  font-family: noah;
}
#text {
  font-weight: 500;
}
</style>
