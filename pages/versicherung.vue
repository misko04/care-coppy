<script setup>
definePageMeta({
  layout: false,
});
</script>

<template>
  <head>
    <link href="https://fonts.cdnfonts.com/css/noah" rel="stylesheet" />
  </head>
  <div>
    <NuxtLayout name="navbar-dark">
      <div class="w-full h-[48px] md:h-[64px] xl:h-[96px]"></div>
      <section>
        <div
          class="w-full px-[24px] mx-auto md:px-[48px] md:max-w-[calc(672px+48px+48px)] xl:max-w-[calc(986px+48px+48px)] text-center content-center"
        >
          <p class="text-base font-semibold text-blue-600 xl:text-lg">
            Anerkannt von Zusatzversicherungen
          </p>
          <div class="w-full h-[16px] xl:h-[24px]"></div>
          <h1
            class="text-4xl font-semibold text-gray-900 md:text-5xl xl:text-6xl"
          >
            Profitiere von deiner Zusatzversicherung
          </h1>
          <div class="w-full h-[16px] md:h-[24px] xl:h-[32px]"></div>
          <div
            class="text-base font-500 xl:text-lg text-center text-gray-500 items-center flex justify-center"
          >
            <p class="max-w-[578px]">
              Fülle dieses Formular aus und erhalte eine E-Mail mit einem
              Kostenvoranschlag, den du an deine Krankenversicherung sendens
              kannst.
            </p>
          </div>
        </div>
      </section>
      <div class="w-full h-[32px] md:h-[48px] xl:h-[64px]"></div>
      <section>
        <div
          class="w-full px-[24px] mx-auto md:px-[48px] md:max-w-[calc(672px+48px+48px)] xl:max-w-[calc(1188px+48px+48px)]"
        >
          <div class="mx-auto w-fit max-w-full md:max-w-[983px]">
            <div
              class="swiper swiper-initialized swiper-horizontal w-full overflow-x-hidden transition-opacity duration-300 opacity-100 swiper-backface-hidden"
            >
              <div class="flex justify-between">
                <div class="h-[48px] px-[12px]">
                  <img
                    class="inline-block h-full w-full inner-img:h-full inner-img:w-full inner-img:object-contain"
                    src="/assets/helsana.webp"
                    alt=""
                  />
                </div>
                <div class="h-[48px] px-[12px]">
                  <img
                    class="inline-block h-full w-full inner-img:h-full inner-img:w-full inner-img:object-contain"
                    src="/assets/swca.webp"
                    alt=""
                  />
                </div>
                <div class="h-[48px] px-[12px]">
                  <img
                    class="inline-block h-full w-full inner-img:h-full inner-img:w-full inner-img:object-contain"
                    src="/assets/css.webp"
                    alt=""
                  />
                </div>
                <div class="h-[48px] px-[12px]">
                  <img
                    class="inline-block h-full w-full inner-img:h-full inner-img:w-full inner-img:object-contain"
                    src="/assets/sanitas.webp"
                    alt=""
                  />
                </div>

                <div class="h-[48px] px-[12px]">
                  <img
                    class="inline-block h-full w-full inner-img:h-full inner-img:w-full inner-img:object-contain"
                    src="/assets/axa.webp"
                    alt=""
                  />
                </div>
                <div class="h-[48px] px-[12px]">
                  <img
                    class="inline-block h-full w-full inner-img:h-full inner-img:w-full inner-img:object-contain"
                    src="/assets/kpt.webp"
                    alt=""
                  />
                </div>
                <div class="h-[48px] px-[12px]">
                  <img
                    class="inline-block h-full w-full inner-img:h-full inner-img:w-full inner-img:object-contain"
                    src="/assets/visana.webp"
                    alt=""
                  />
                </div>
                <div class="h-[48px] px-[12px]">
                  <img
                    class="inline-block h-full w-full inner-img:h-full inner-img:w-full inner-img:object-contain"
                    src="/assets/sympany.webp"
                    alt=""
                  />
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="w-full h-[32px] md:h-[64px]"></div>
        <form action="" class="m-auto block w-full xl:max-w-[577px]">
          <div
            class="grid grid-cols-1 gap-[16px] md:grid-cols-2 xl:grid-cols-1"
          >
            <div class="space-y-[8px]">
              <div class="relative">
                <select
                  name="checkup"
                  id=""
                  class="w-full appearance-none rounded-[8px] border border-gray-200 bg-white px-[16px] py-[12px] text-lg font-500 text-gray-900 focus:outline-none"
                >
                  <option value="Wähle deinen Check-up">
                    Wähle deinen Check-up
                  </option>
                  <option value="Wähle deinen Check-up">
                    Wähle deinen Check-up
                  </option>
                  <option value="Wähle deinen Check-up">
                    Wähle deinen Check-up
                  </option>
                </select>
                <div
                  class="absolute right-[12px] top-[23px] transition-transform w-[10px] flex items-center"
                >
                  <img src="/assets/down-gray.png" alt="" />
                </div>
              </div>
            </div>
            <div class="space-y-[8px]">
              <input
                type="text"
                placeholder="Vorname"
                name="firstName"
                class="w-full appearance-none rounded-[8px] border border-gray-200 bg-white px-[16px] py-[12px] text-lg font-500 text-gray-900 focus:outline-none"
              />
            </div>
            <div class="space-y-[8px]">
              <input
                type="text"
                placeholder="Nachname"
                class="w-full appearance-none rounded-[8px] border border-gray-200 bg-white px-[16px] py-[12px] text-lg font-500 text-gray-900 focus:outline-none"
              />
            </div>
            <div class="space-y-[8px]">
              <input
                type="email"
                placeholder="Deine E-Mail"
                class="w-full appearance-none rounded-[8px] border border-gray-200 bg-white px-[16px] py-[12px] text-lg font-500 text-gray-900 focus:outline-none"
              />
            </div>
          </div>
          <div class="w-full h-[32px] md:h-[64px]"></div>
          <div class="flex justify-center">
            <button
              class="block bg-blue-600 text-white rounded-full py-[11px] px-[23px]"
            >
              Kostenvoranschlag senden
            </button>
          </div>
        </form>
        <div class="w-full h-[32px] md:h-[64px]"></div>
      </section>
      <section>
        <listPicker></listPicker>
      </section>
      <div class="w-full h-[48px] md:h-[64px] xl:h-[128px]"></div>

      <section>
        <div
          class="w-full px-[24px] mx-auto md:px-[48px] md:max-w-[calc(672px+48px+48px)] xl:max-w-[calc(968px+48px+48px)] relative"
        >
          <div
            class="bg-blue-600 relative isolate mx-auto min-h-[592px] overflow-hidden rounded-[24px] px-[24px] md:grid md:min-h-[282px] md:grid-cols-2 md:gap-x-[24px] md:px-[48px] xl:min-h-[385px] xl:max-w-none xl:px-[64px]"
          >
            <div
              class="flex flex-col items-center justify-center md:items-start"
            >
              <div class="w-full h-[48px] xl:h-[112px]"></div>
              <h3
                class="text-white text-3xl xl:text-4xl text-center md:text-left font-bold"
              >
                Beginne heute deine Gesundheit besser zu verstehen
              </h3>
              <div class="w-full h-[32px] xl:h-[28px]"></div>
              <div
                class="flex flex-cols items-center justify-start gap-[18px] md:gap-[24px]"
              >
                <a
                  class="block max-w-max rounded-full text-center relative border bg-white border-white py-[11px] px-[25px]"
                  >Check-up buchen</a
                >
              </div>
              <div class="w-full h-[21px] md:h-[46px] xl:h-[112px]"></div>
            </div>
            <div
              class="mx-[-24px] mb-[-40px] mt-[16px] flex h-[336px] min-h-[336px] translate-x-[12px] scale-[1.3] flex-col items-center justify-end md:absolute md:bottom-[-60px] md:right-[-34px] md:top-0 md:m-0 md:mb-0 md:mt-0 md:translate-x-0 xl:bottom-[-114px] xl:right-[-150px] xl:scale-[2.2]"
            >
              <img class="overflow-hidden" src="/assets/women.webp" alt="" />
            </div>
          </div>
        </div>
      </section>
      <div class="w-full h-[48px] md:h-[64px] xl:h-[128px]"></div>
      <section>
        <div
          class="w-full px-[24px] mx-auto md:px-[48px] md:max-w-[calc(672px+48px+48px)] xl:max-w-[calc(1188px+48px+48px)] relative"
        >
          <div
            class="gap-x-[24px] gap-y-[32px] md:gap-y-[48px] xl:gap-x-[32px] md:grid-cols-2 xl:grid-cols-2 grid-cols-1 grid"
          >
            <div class="w-full rounded-[16px] bg-gray-50 p-[32px]">
              <div class="flex items-center gap-x-[24px]">
                <h3 class="font-bold flex-1">Schreibe uns eine E-Mail</h3>
                <div class="w-[24px] h-[24px]">
                  <img src="/assets/icon-mail-blue.svg" alt="" />
                </div>
              </div>
              <div class="w-full h-[24px]"></div>
              <div>
                <p class="font-bold underline">hello@care.me</p>
                <p class="font-bold text-gray-500 text-lg">
                  Wir antworten normalerweise innerhalb von 24 Stunden.
                </p>
              </div>
            </div>
            <div class="w-full rounded-[16px] bg-gray-50 p-[32px]">
              <div class="flex items-center gap-x-[24px]">
                <h3 class="font-bold flex-1">Schreibe uns eine E-Mail</h3>
                <div class="w-[24px] h-[24px]">
                  <img src="/assets/icon-mail-blue.svg" alt="" />
                </div>
              </div>
              <div class="w-full h-[24px]"></div>
              <div>
                <p class="font-bold underline">hello@care.me</p>
                <p class="font-bold text-gray-500 text-lg">
                  Wir antworten normalerweise innerhalb von 24 Stunden.
                </p>
              </div>
            </div>
          </div>
        </div>
      </section>
      <div class="w-full h-[48px] md:h-[64px] xl:h-[128px]"></div>
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
                  h3="Wann habe ich Anspruch auf eine Rückerstattung?"
                  message="Die Erstattung deines CARE Abos hängt von deiner spezifischen Zusatzversicherung ab. Gerne beraten wir dich."
                ></Unfoldable>
              </li>
              <li>
                <Unfoldable
                  h3="Wann erhalte ich meine Rückerstattung?"
                  message="Du erhältst die Rückerstattung von deiner Versicherung innerhalb des üblichen Bearbeitungszeitraums."
                ></Unfoldable>
              </li>
              <li>
                <Unfoldable
                  h3="Haben bestehende Mitglieder Anspruch auf eine Erstattung?"
                  message="Ja, falls du deinen Rückforderungsbeleg noch nicht eingereicht hast, erstattet dir deine Versicherung die Kosten, auch wenn du bereits Mitglied bist. Reiche hierzu deinen Rückforderungsbeleg bei deiner Versicherung ein."
                ></Unfoldable>
              </li>
              <li>
                <Unfoldable
                  h3="Welche Versicherungen erstatten die Kosten vom CARE Abo?"
                  message="Viele der grossen Schweizer Versicherungen übernehmen ein Teil des CARE Abos. Reiche einen Kostenvoranschlag bei deiner Versicherung ein und erfahre, wie viel erstattet wird."
                ></Unfoldable>
              </li>
              <li>
                <Unfoldable
                  h3="Wie viel bekomme ich von meiner Zusatzversicherung zurückerstattet?"
                  message="Das hängt von deiner spezifischen Zusatzversicherung ab. In den meisten Fällen erhalten unsere Mitglieder eine Rückerstattung von CHF 300 bis 1’000."
                ></Unfoldable>
              </li>
              <li>
                <Unfoldable
                  h3="Ich habe keine Zusatzversicherung, zahlt meine normale Versicherung?"
                  message="Präventionsmassnahmen (wie ein Check-up) werden üblicherweise nur von der Zusatzversicherung übernommen. Für genaue Informationen wende dich bitte an deine Versicherung."
                ></Unfoldable>
              </li>
              <li>
                <Unfoldable
                  h3="Wie häufig erhalte ich eine Rückerstattung?"
                  message="In der Regel erhältst du jährlich eine Rückerstattung. Die Frequenz der Rückerstattungen hängt von deiner Zusatzversicherung ab."
                ></Unfoldable>
              </li>
            </ul>
          </div>
        </div>
      </div>
      <div class="w-full h-[48px] md:h-[64px] xl:h-[128px]"></div>
    </NuxtLayout>
  </div>
</template>
