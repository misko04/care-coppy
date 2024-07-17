<template>
  <head>
    <link href="https://fonts.cdnfonts.com/css/noah" rel="stylesheet" />
  </head>

  <NuxtLayout name="navbar-dark" v-editable="block">
    <div class="w-full h-[48px] md:h-[64px] xl:h-[96px]"></div>
    <section>
      <div
        class="w-full px-[24px] mx-auto md:px-[48px] md:max-w-[calc(672px+48px+48px)] xl:max-w-[calc(986px+48px+48px)] text-center"
      >
        <p class="text-base font-semibold text-blue-600 xl:text-lg">
          So funktioniert's
        </p>
        <div class="w-full h-[16px] xl:h-[24px]"></div>
        <h1
          class="text-4xl font-semibold text-gray-900 md:text-5xl xl:text-6xl"
        >
          Verlängere deine Lebenserwartung schrittweise
        </h1>
        <div class="w-full h-[16px] xl:h-[24px]"></div>
        <p
          class="text-gray-500 mx-auto text-base md:text-lg xl:text-xl max-w-[672px] xl:max-w-[780px] font-medium"
        >
          Erhalte eine ausführliche Analyse deines gesamten Körpers für einen
          umfassenden Einblick in deine Gesundheit.
        </p>
      </div>
    </section>
    <div class="w-full h-[100px] md:h-[144px] xl:h-[196px]"></div>
    <section class="bg-white">
      <div class="relative mx-auto md:max-w-[672px] xl:max-w-[986px]">
        <div
          class="h-[196px] w-full overflow-hidden md:h-[200px] md:rounded-[16px] xl:h-[248px] xl:rounded-[24px]"
        >
          <picture class="overflow-hidden">
            <img
              class="w-full h-full object-cover"
              src="/assets/wave-bg.webp"
              alt=""
            />
          </picture>
        </div>
        <div
          class="absolute inset-x-0 bottom-0 mx-auto h-[240px] w-[348px] md:h-[280px] md:w-[406px] xl:h-[350px] xl:w-[508px]"
        >
          <picture class="overflow-hidden">
            <img
              class="w-full h-full object-contain"
              src="/assets/man-bg.webp"
              alt=""
            />
          </picture>
        </div>
      </div>
    </section>
    <div class="w-full h-[48px] md:h-[64px] xl:h-[128px]"></div>
    <section>
      <div class="mx-auto px-[24px] md:max-w-[672px] md:px-0 xl:max-w-[986px]">
        <h2 class="text-center text-2xl font-bold md:text-3xl xl:text-4xl">
          4 einfache Schritte zu besserer Gesundheit
        </h2>
        <div class="w-full h-[32px] md:h-[50px] xl:h-[48px]"></div>
        <div
          class="grid grid-cols-1 gap-[32px] gap-x-[24px] md:grid-cols-2 md:gap-y-[50px] xl:grid-cols-4"
        >
          <blocksNumFunk
            num="1"
            h3-msg="Buche einen Check-up"
            p-msg="Finde einen Termin und buche deinen CARE Check-up bequem über unsere Website."
          ></blocksNumFunk>
          <blocksNumFunk
            num="2"
            h3-msg="Erhalte personalisierte Einblicke"
            p-msg="Besprich deine Ergebnisse mit ärztlichem Fachpersonal und/oder einem Gesundheitscoach und lasse dich individuell zu deiner Gesundheit beraten."
          ></blocksNumFunk>
          <blocksNumFunk
            num="3"
            h3-msg="Tracke deine Gesundheit digital"
            p-msg="Mit unserer nutzerfreundlichen App kannst du ganz einfach auf deine Gesundheitsdaten zugreifen, deine Fortschritte verfolgen und Empfehlungen erhalten."
          ></blocksNumFunk>
          <blocksNumFunk
            num="4"
            h3-msg="Steigere deine Gesundheitsreise"
            p-msg="Du hast die Möglichkeit, noch mehr an deiner Gesundheit zu arbeiten, indem du zusätzliche Blutuntersuchungen, Herz- und Atemtests, Coachings oder Nahrungsergänzungsmittel in Anspruch nimmst."
          ></blocksNumFunk>
        </div>
      </div>
    </section>
    <div class="w-full h-[48px] md:h-[64px] xl:h-[128px]"></div>
    <section class="bg-neutral-900">
      <div class="w-full h-[48px] md:h-[64px] xl:h-[128px]"></div>
      <div class="mx-auto px-[24px] md:max-w-[672px] md:px-0 xl:max-w-[986px]">
        <div class="flex flex-col items-center text-center">
          <h1 class="text-white text-center text-4xl font-bold">
            Bereit für eine Veränderung?
          </h1>
          <div class="w-full h-[32px] xl:h-[48px]"></div>
          <div class="justify-start gap-[18px] md:gap-[24px]">
            <a
              class="block cursor-pointer max-w-max rounded-full text-center relative bg-blue-600 py-[11px] px-[25px] text-white"
              >Check-up buchen</a
            >
          </div>
        </div>
      </div>
      <div class="w-full h-[48px] md:h-[64px] xl:h-[128px]"></div>
    </section>
    <div class="w-full h-[48px] md:h-[64px] xl:h-[128px]"></div>
    <section>
      <div
        class="w-full px-[24px] mx-auto md:px-[48px] md:max-w-[calc(672px+48px+48px)] xl:max-w-[calc(986px+48px+48px)]"
      >
        <PictureTextBolck
          order="md:order-2"
          img="care-women.webp"
          h3text="Früherkennung und Prävention von Krankheiten"
          ptext="Unsere CARE Check-ups helfen dir, deine Gesundheit zu überwachen und zu optimieren, indem du auf vier wichtige Säulen zugreifst: Blut, Herz, Ausdauer und Lebensstil. Erkenne und verhindere Krankheiten im Frühstadium, bevor sie sich zu dauerhaften Problemen entwickeln."
        ></PictureTextBolck>
        <div class="w-full h-[48px] md:h-[64px] xl:h-[128px]"></div>
        <PictureTextBolck
          order="md:order-1"
          img="care-talk.webp"
          h3text="Personalisierte Beratung und Betreuung durch ärztliches Fachpersonal sowie Health Coaches"
          ptext="Unser medizinisches Team widmet sich voll und ganz deiner Gesundheit und wird dich dabei unterstützen, deine Ergebnisse zu verstehen, die richtigen Ergänzungsmittel zu empfehlen und die beste CARE-Reise für dich zu definieren."
        ></PictureTextBolck>
        <div class="w-full h-[48px] md:h-[64px] xl:h-[128px]"></div>
        <PictureTextBolck
          order="md:order-2"
          img="care-pc.webp"
          h3text="Effektive Selbstoptimierung durch neue Gewohnheiten"
          ptext="Profitiere von dem Wissen unserer Gesundheitsexperten in den Bereichen Ernährung, Bewegung, Schlaf und Stressmanagement. Besonders geeignet für gezielte Ernährungsumstellung, Gewichtszunahme oder -reduktion sowie Muskelaufbau."
        ></PictureTextBolck>
        <div class="w-full h-[48px] md:h-[64px] xl:h-[128px]"></div>
        <PictureTextBolck
          order="md:order-1"
          img="care-phone.webp"
          h3text="Digitaler Zugang zu deiner Gesundheit mit der CARE App"
          ptext="Tracke deinen CARE Score, greife auf deine Ergebnisse und Berichte zu und erhalte individuelle Beratung von unserem KI-Coach. All das wird von unserem Produkt-Team, unseren internen Wissenschafter und unserem medizinischen Team sorgfältig bereitgestellt."
        ></PictureTextBolck>
      </div>
    </section>
    <div class="w-full h-[48px] md:h-[64px] xl:h-[128px]"></div>
    <div class="w-full h-[48px] md:h-[64px] xl:h-[128px] bg-neutral-900"></div>
    <section class="bg-neutral-900">
      <div
        class="w-full px-[24px] mx-auto md:px-[48px] md:max-w-[calc(672px+48px+48px)] xl:max-w-[calc(1188px+48px+48px)]"
      >
        <div
          class="grid grid-cols-1 gap-y-[32px] md:grid-cols-2 md:items-center md-gap-x-[24px] xl:grid-cols-12"
        >
          <div id="pic" class="md:order-2 xl:col-span-4 xl:h-[578px]">
            <picture class="overflow-hidden aspect-square">
              <img
                class="w-full h-full object-cover"
                src="/assets/care-3-pics.webp"
                alt=""
              />
            </picture>
          </div>
          <div
            id="text"
            class="space-y-[12px] md:order-1 md:space-y-[16px] md:pr-[24px] xl:col-span-6 xl:col-start-2 xl:pr-[64px]"
          >
            <h3 class="font-bold text-3xl xl:text-4xl text-white">
              Die Zukunft der Medizin
            </h3>
            <div class="text-base xl:text-lg">
              <p class="text-white">
                Investiere in dich selbst und stelle deine persönliche
                Gesundheitsreise in den Vordergrund. Ändere deine Gewohnheiten
                Schritt für Schritt und verbessere deine Lebensqualität
                langfristig.
              </p>
            </div>
          </div>
        </div>
      </div>
    </section>
    <div class="w-full h-[48px] md:h-[64px] xl:h-[128px] bg-neutral-900"></div>
    <div class="w-full h-[48px] md:h-[64px] xl:h-[128px]"></div>
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
                  h3="Wo wird mir das Blut abgenommen?"
                  message="Die Erstattung deines CARE Abos hängt von deiner spezifischen Zusatzversicherung ab. Gerne beraten wir dich."
                ></Unfoldable>
              </li>
              <li>
                <Unfoldable
                  h3="Was bedeutet mein CARE Score?"
                  message="Die Erstattung deines CARE Abos hängt von deiner spezifischen Zusatzversicherung ab. Gerne beraten wir dich."
                ></Unfoldable>
              </li>
              <li>
                <Unfoldable
                  h3="Wie und wann erhalte ich meine Ergebnisse?"
                  message="Die Erstattung deines CARE Abos hängt von deiner spezifischen Zusatzversicherung ab. Gerne beraten wir dich."
                ></Unfoldable>
              </li>
              <li>
                <Unfoldable
                  h3="Welche Art von Service werden angeboten?"
                  message="Die Erstattung deines CARE Abos hängt von deiner spezifischen Zusatzversicherung ab. Gerne beraten wir dich."
                ></Unfoldable>
              </li>
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
              <li>
                <Unfoldable
                  h3="Wie alt muss ich sein, um das Angebot von CARE zu nutzen?"
                  message="Die Erstattung deines CARE Abos hängt von deiner spezifischen Zusatzversicherung ab. Gerne beraten wir dich."
                ></Unfoldable>
              </li>
              <li>
                <Unfoldable
                  h3="Welche Zahlungsarten werden von CARE akzeptiert?"
                  message="Die Erstattung deines CARE Abos hängt von deiner spezifischen Zusatzversicherung ab. Gerne beraten wir dich."
                ></Unfoldable>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </section>
    <div class="w-full h-[48px] md:h-[64px] xl:h-[128px]"></div>
  </NuxtLayout>
</template>

<script setup>
definePageMeta({
  layout: false,
});
defineProps({
  block: {},
});
</script>

<style>
#text {
  @media (min-width: 1408px) {
    grid-column-start: 1;
  }
}
#pic {
  @media (min-width: 1408px) {
    grid-column: span 6 / span 6;
  }
}
</style>
