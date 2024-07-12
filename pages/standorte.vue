<template>
  <head>
    <link href="https://fonts.cdnfonts.com/css/noah" rel="stylesheet" />
  </head>
  <NuxtLayout name="navbar-dark">
    <div class="w-full h-[48px] md:h-[64px] xl:h-[96px]"></div>
    <section>
      <div
        class="w-full px-[24px] mx-auto md:px-[48px] md:max-w-[calc(672px+48px+48px)] xl:max-w-[calc(986px+48px+48px)] text-center"
      >
        <p class="text-base font-semibold text-blue-600 xl:text-lg">
          Besuche CARE
        </p>
        <div class="w-full h-[16px] xl:h-[24px]"></div>
        <h1
          class="text-4xl font-semibold text-gray-900 md:text-5xl xl:text-6xl"
        >
          Unsere Standorte
        </h1>
        <div class="w-full h-[16px] xl:h-[24px]"></div>
        <p
          class="text-gray-500 mx-auto text-base md:text-lg xl:text-xl max-w-[672px] xl:max-w-[780px] font-medium"
        >
          Entdecke die CARE Angebote in unserem Flagship Store oder bei einem
          unserer zuverlässigen Partnern.
        </p>
      </div>
    </section>
    <div class="w-full h-[48px] md:h-[64px] xl:h-[96px]"></div>
    <section>
      <div
        class="w-full px-[24px] mx-auto md:px-[48px] md:max-w-[calc(672px+48px+48px)] xl:max-w-[calc(1188px+48px+48px)]"
      >
        <div
          class="grid grid-cols-1 gap-x-[24px] gap-y-[32px] md:gap-y-[48px] xl:gap-x-[32px] md:grid-cols-1 xl:grid-cols-3"
        >
          <CityBolck
            city="Zürich"
            address="Seestrasse 7, 8002 Zürich"
            openh="Mo - Sa: 08:00 - 18:00"
            mail="hello@care.me"
            phone="+41 44 500 8390"
            hiden=""
            ptext=""
          ></CityBolck>
          <CityBolck
            city="Bern"
            address="Aarbergergasse 21, 3011 Bern"
            openh="Di - Do: 07:00 - 09:30"
            mail="bern@care.me"
            phone="+41 44 500 8390"
            hiden="hidden"
            ptext="c/o Hair & Skin Bern"
          ></CityBolck>
          <CityBolck
            city="Basel"
            address="Klybeckstrasse 140, 4057 Basel"
            openh="Mo - Fr: 08:30 - 12:00"
            mail="basel@care.me"
            phone="+44 500 75 72"
            hiden="hidden"
            ptext="c/o Dreirosen Apotheke"
          ></CityBolck>
          <CityBolck
            city="Luzern"
            address="Alpenquai 30, 6005 Luzern"
            openh="Di - Do: 08:00 - 10:00"
            mail="luzern@care.me"
            phone="+44 500 75 72"
            hiden="hidden"
            ptext="c/o Future Medicine Clinic"
          ></CityBolck>
        </div>
      </div>
    </section>
    <div class="w-full h-[24px] md:h-[24px] xl:h-[24px]"></div>
    <div class="w-full h-[24px] md:h-[48px] xl:h-[64px]"></div>
    <section>
      <div
        class="w-full px-[24px] mx-auto md:px-[48px] md:max-w-[calc(672px+48px+48px)] xl:max-w-[calc(1188px+48px+48px)] text-center"
      >
        <div
          class="swiper swiper-fade swiper-initialized swiper-horizontal swiper-watch-progress h-[192px] w-full md:h-[378px] xl:h-[480px] swiper-backface-hidden"
        >
          <picture class="w-full h-full">
            <img
              class="w-full h-full object-cover rounded-[16px]"
              src="/assets/care-office.webp"
              alt=""
            />
          </picture>
        </div>
      </div>
    </section>
    <div class="w-full h-[48px] md:h-[64px] xl:h-[96px]"></div>
    <section>
      <standoreListBlock></standoreListBlock>
    </section>
    <div class="w-full h-[48px] md:h-[64px] xl:h-[96px]"></div>
    <section class="bg-black">
      <div class="w-full h-[48px] md:h-[64px] xl:h-[96px]"></div>
      <div
        class="w-full px-[24px] mx-auto md:px-[48px] md:max-w-[calc(672px+48px+48px)] xl:max-w-[calc(986px+48px+48px)] text-center"
      >
        <h3
          class="font-bold text-center text-white text-2xl md:text-3xl xl:text-4xl"
        >
          Ein interdisziplinäres Team von Ärzt:innen und Health Coaches
        </h3>
      </div>
      <div class="w-full h-[32px] md:h-[48px] xl:h-[64px]"></div>
      <div class="flex-col flex items-center">
        <div
          class="w-full px-[24px] mx-auto md:px-[48px] md:max-w-[calc(672px+48px+48px)] xl:max-w-[calc(1188px+48px+48px)] flex justify-center"
        >
          <div
            class="flex overflow-x-auto flex-nowrap no-scroll-thumb rounded-full p-[4px] w-fit bg-neutral-800"
          >
            <button
              @click="arzteSet"
              class="outline-none duration-250 w-content shrink-0 rounded-full py-[8px] px-[16px] transition-colors text-sm font-700 leading-[20px] text-white"
              :class="{ 'bg-blue-600': arzte }"
            >
              Ärzte
            </button>
            <button
              @click="healthSet"
              class="outline-none duration-250 w-content shrink-0 rounded-full py-[8px] px-[16px] transition-colors text-sm font-700 leading-[20px] text-white"
              :class="{ 'bg-blue-600': health }"
            >
              Health Coaches
            </button>
            <button
              @click="mpasSet"
              class="outline-none duration-250 w-content shrink-0 rounded-full py-[8px] px-[16px] transition-colors text-sm font-700 leading-[20px] text-white"
              :class="{ 'bg-blue-600': mpas }"
            >
              MPAs
            </button>
          </div>
        </div>
        <div
          class="w-full px-[24px] mx-auto md:px-[48px] md:max-w-[calc(672px+48px+48px)] xl:max-w-[calc(1188px+48px+48px)]"
        >
          <div class="w-full h-[32px] md:h-[48px] xl:h-[64px]"></div>
          <div
            class="gap-x-[24px] gap-y-[32px] md:gap-y-[48px] xl:gap-x-[32px] md:grid-cols-2 xl:grid-cols-3 grid-cols-1 grid text-white"
            v-if="arzte"
          >
            <DoctorsCards
              img="mundackal"
              h3-msg="Dr. med. Robert Mundackal"
              p-msg="Medical lead/ Ärztlicher Leiter, Facharzt für Allgemeine und Innere Medizin und Facharzt für Pneumologie mit Schwerpunkt Schlafmedizin und Notfallmedizin"
            ></DoctorsCards>
            <DoctorsCards
              img="dobosi"
              h3-msg="Dr. med. Andrea Dobosi"
              p-msg="Fachärztin für Gynäkologie und Geburtshilfe mit Spezialgebiet weibliche Hormone"
            ></DoctorsCards>
            <DoctorsCards
              img="walser"
              h3-msg="Dr. med. Roman Walser"
              p-msg="Facharzt für Allgemeine- und Innere Medizin mit Schwerpunkt Sport- und Trainingsmedizin"
            ></DoctorsCards>
            <DoctorsCards
              img="jakob"
              h3-msg="Dr. med. Bernd Jakob"
              p-msg="Facharzt für Orthopädie und Unfallchirurgie mit Schwerpunkten in Sportmedizin und Notfallmedizin"
            ></DoctorsCards>
          </div>

          <!-- --------------------------------------------------------------- -->

          <div
            class="gap-x-[24px] gap-y-[32px] md:gap-y-[48px] xl:gap-x-[32px] md:grid-cols-2 xl:grid-cols-3 grid-cols-1 grid text-white"
            v-if="health"
          >
            <DoctorsCards
              img="arnet"
              h3-msg="Patrick Arnet"
              p-msg="Bewegungswissenschaften und Sport MSc, ETH"
            ></DoctorsCards>
            <DoctorsCards
              img="bernet"
              h3-msg="Jris Bernet"
              p-msg="Gesundheitsberaterin AKN, spezialisiert auf Stoffwechselstörungen und zertifizierter Schlafcoach"
            ></DoctorsCards>

            <DoctorsCards
              img="pongracz"
              h3-msg="Kata Pongracz"
              p-msg="Sport-, Ernährungs- und Life-Coach (Stressmanagement)"
            ></DoctorsCards>
            <DoctorsCards
              img="miranda"
              h3-msg="Noemi Miranda"
              p-msg="Health Coach mit Spezialisierung auf Sportmanagement"
            ></DoctorsCards>
            <DoctorsCards
              img="lagovitina"
              h3-msg="Elena Iagovitina"
              p-msg="Health Coach und Community Lead"
            ></DoctorsCards>
            <DoctorsCards
              img="avatar"
              h3-msg="Willow Gahm"
              p-msg="Health Coach mit Spezialisierung in klinischer Psychologie, BA Harvard University"
            ></DoctorsCards>
          </div>

          <!-- --------------------------------------------------------------- -->

          <div
            class="gap-x-[24px] gap-y-[32px] md:gap-y-[48px] xl:gap-x-[32px] md:grid-cols-2 xl:grid-cols-3 grid-cols-1 grid text-white"
            v-if="mpas"
          >
            <DoctorsCards
              img="hassan"
              h3-msg="Haia Hassan"
              p-msg="Store Lead"
            ></DoctorsCards>
            <DoctorsCards
              img="dam"
              h3-msg="Melody Dam"
              p-msg="Medizinische Praxisassistentin"
            ></DoctorsCards>
            <DoctorsCards
              img="pjetraj"
              h3-msg="Arbentina Pjetraj"
              p-msg="Medizinische Praxisassistentin"
            ></DoctorsCards>
            <DoctorsCards
              img="ramadani"
              h3-msg="Almir Ramadani"
              p-msg="Medizinischer Praxisassistent"
            ></DoctorsCards>
            <DoctorsCards
              img="avatar"
              h3-msg="Nicole Huser"
              p-msg="Medizinische Praxisassistentin"
            ></DoctorsCards>
            <DoctorsCards
              img="avatar"
              h3-msg="Lauxna Thavarajasekaram"
              p-msg="Medizinische Praxisassistentin"
            ></DoctorsCards>
          </div>

          <!-- --------------------------------------------------------------- -->
        </div>
      </div>

      <div class="w-full h-[48px] md:h-[64px] xl:h-[96px]"></div>
    </section>
    <div class="w-full h-[48px] md:h-[64px] xl:h-[96px]"></div>
    <section>
      <div
        class="w-full px-[24px] mx-auto md:px-[48px] md:max-w-[calc(672px+48px+48px)] xl:max-w-[calc(1188px+48px+48px)]"
      >
        <div
          class="rouded-[24px] bg-black w-full h-full overflow-hidden rounded-[24px]"
        >
          <div class="flex flex-col md:flex-row">
            <div
              class="h-1/2 flex flex-col justify-center px-[16px] py-[32px] text-center md:h-auto md:w-1/2 md:items-start md:py-[48px] md:pl-[48px] md:pr-[28px] md:text-left xl:py-[64px] xl:pl-[64px] xl:pr-[32px]"
            >
              <h3 class="font-bold text-2xl md:text-3xl xl:text-4xl text-white">
                Entdecke unsere Angebote der Präventivmedizin
              </h3>
              <div class="w-full h-[8px]"></div>
              <p class="text-base font-medium xl:text-lg text-white">
                Von umfassenden Bluttests, über Analysen deiner
                Körperzusammensetzung hinzu VO2 Max Messungen bietet CARE dir
                diverse Untersuchungen für deine Gesundheit.
              </p>
              <div class="w-full h-[32px] md:h-[48px] xl:h-[64px]"></div>
              <div
                class="flex flex-cols items-center justify-start gap-[18px] md:gap-[24px]"
              >
                <a
                  class="block max-w-max rounded-full text-center relative border bg-white border-white py-[11px] px-[25px]"
                >
                  Entdecke unsere Services</a
                >
              </div>
            </div>
            <div>
              <img src="/assets/man-veins.webp" alt="" />
            </div>
          </div>
        </div>
      </div>
    </section>
    <div class="w-full h-[48px] md:h-[64px] xl:h-[96px]"></div>
    <section>
      <div
        class="w-full px-[24px] mx-auto md:px-[48px] md:max-w-[calc(672px+48px+48px)] xl:max-w-[calc(1188px+48px+48px)]"
      >
        <div class="grid xl:grid-cols-12">
          <div
            class="space-y-[32px] md:space-y-[48px] xl:col-start-3 xl:col-end-11 xl:space-y-[64px]"
          >
            <h1 class="text-4xl font-bold">Häufige Fragen</h1>
            <ul class="space-y-[16px]">
              <li>
                <Unfoldable
                  h3="Wie soll ich mich auf die Blutentnahme vorbereiten?"
                  message="Die Erstattung deines CARE Abos hängt von deiner spezifischen Zusatzversicherung ab. Gerne beraten wir dich."
                ></Unfoldable>
              </li>
              <li>
                <Unfoldable
                  h3="Was soll ich tun, wenn ich meinen Termin nicht wahrnehmen kann?"
                  message="Die Erstattung deines CARE Abos hängt von deiner spezifischen Zusatzversicherung ab. Gerne beraten wir dich."
                ></Unfoldable>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </section>
    <div class="w-full h-[48px] md:h-[64px] xl:h-[96px]"></div>
  </NuxtLayout>
</template>

<script setup>
var arzte = ref(true);
var health = ref(false);
var mpas = ref(false);

function arzteSet() {
  arzte.value = true;
  health.value = false;
  mpas.value = false;
}

function healthSet() {
  health.value = true;
  arzte.value = false;
  mpas.value = false;
}

function mpasSet() {
  health.value = false;
  arzte.value = false;
  mpas.value = true;
}

definePageMeta({
  layout: false,
});
</script>
