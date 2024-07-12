<template>
  <header
    class="relative inset-x-0 top-0 z-[100] bg-transparent transition-transform duration-300"
  >
    <div
      class="w-full px-[24px] mx-auto md:px-[48px] md:max-w-[calc(672px+48px+48px)] xl:max-w-[calc(1290px+48px+48px)]"
    >
      <div
        class="flex min-h-[64px] items-center justify-between py-[16px] xl:py-[42px]"
      >
        <div class="flex items-center gap-[] text-white">
          <NuxtLink
            to="/"
            class="h-[20px] w-[72px] xl:h-[24px] xl:w-[86px] bg-white"
          >
          </NuxtLink>
        </div>
        <nav class="hidden xl:block">
          <ul
            class="!text-white flex items-center justify-betweeen space-x-[32px]"
          >
            <NuxtLink
              href="/sofunk"
              class="block max-w-max w-full text-center font-500 duration-300 relative border border-transparent bg-transparent"
            >
              <p id="p" v-if="language">So funktioniert's</p>
              <p id="p" v-if="!language">How it works</p>
            </NuxtLink>
            <NuxtLink
              to="/preise"
              class="block max-w-max w-full text-center font-500 duration-300 relative border border-transparent bg-transparent"
            >
              <p id="p" v-if="language">Preise</p>
              <p id="p" v-if="!language">Pricing</p>
            </NuxtLink>
            <NuxtLink
              to="/versicherung"
              class="block max-w-max w-full text-center font-500 duration-300 relative border border-transparent bg-transparent"
              ><p id="p" v-if="language">Versicherung</p>
              <p id="p" v-if="!language">Insurance</p>
            </NuxtLink>
            <NuxtLink
              to="/standorte"
              class="block max-w-max w-full text-center font-500 duration-300 relative border border-transparent bg-transparent"
              ><p id="p" v-if="language">Standorte</p>
              <p id="p" v-if="!language">Locations</p>
            </NuxtLink>
            <div class="relative z-[10] text-left">
              <button
                @click="shownav(), rotate()"
                class="flex items-center space-x-[4px]"
              >
                <span
                  ><p id="p" v-if="language">Mehr</p>
                  <p id="p" v-if="!language">More</p>
                </span>
                <div
                  class="transition-all duration-300"
                  :class="{ ' rotate-[-180deg]': rotate180 }"
                  id="r"
                >
                  <img src="../assets/down-chevron.png" class="w-3" />
                </div>
              </button>
              <ul
                v-show="show"
                class="flex flex-col gap-y-[16px] px-[24px] py-[20px] text-gray-900 xl:absolute xl:left-[-32px] xl:mt-2 xl:w-[200px] xl:rounded-[16px] xl:bg-white xl:shadow-xl"
              >
                <li>
                  <NuxtLink to="/">Blutwerte</NuxtLink>
                </li>
                <li>
                  <NuxtLink to="/">Warum CARE?</NuxtLink>
                </li>
                <li>
                  <NuxtLink to="/">Über CARE</NuxtLink>
                </li>
                <li>
                  <NuxtLink to="/">Member Vorteile</NuxtLink>
                </li>
                <li>
                  <NuxtLink to="/">Praxen & Apotheken</NuxtLink>
                </li>
                <li>
                  <NuxtLink to="/">Blog</NuxtLink>
                </li>
              </ul>
            </div>
          </ul>
        </nav>

        <!----------------------------------------------------->

        <div class="flex items-center space-x-[24px] xl:space-x-[16px]">
          <div
            class="bg-white text-black h-8 rounded-2xl text-sm items-center justify-center text-center py-[6px] px-[12px] font-sans hidden xl:block"
          >
            <a href="https://booking.care.me/ch-de/locations/"
              >Check-up buchen</a
            >
          </div>
          <div class="relative isolate w-max cursor-pointer hidden xl:block">
            <button
              @click="showLgPick"
              class="border rounded-full p-[8px] bg-opacity-0 hover:bg-opacity-20 border-white/20 bg-white transition-all duration-300"
            >
              <img
                src="../assets/icon-globe-light.svg"
                class="w-[14px] h-[14px]"
              />
            </button>
            <div
              @click="
                changeEn();
                showLgPick();
              "
              v-show="languageShow"
              class="top-[40px] md:right-0 absolute z-50 w-max rounded-[8px] border border-gray-200 bg-white p-[8px] transition-all duration-300"
            >
              <div
                class="flex w-full cursor-pointer items-center space-x-[8px] rounded-[8px] px-[8px] py-[4px] transition-all duration-300 active:bg-gray-200 hover:bg-gray-100"
              >
                <div
                  v-show="language"
                  class="h-[15px] w-[20px] shrink-0 overflow-hidden inner-img:object-cover rounded-[4px]"
                >
                  <img class="w-full h-full" src="/assets/icon-en-flag.svg" />
                </div>
                <span
                  v-show="language"
                  class="text-[14px] font-500 leading-[21px] tracking-[0.015em] text-gray-900"
                  >English</span
                >
                <div
                  v-show="!language"
                  class="h-[15px] w-[20px] shrink-0 overflow-hidden inner-img:object-cover rounded-[4px]"
                >
                  <img class="w-full h-full" src="/assets/icon-de-flag.svg" />
                </div>
                <span
                  v-show="!language"
                  class="text-[14px] font-500 leading-[21px] tracking-[0.015em] text-gray-900"
                  >Deutsch</span
                >
              </div>
            </div>
          </div>
          <button class="h-[32px] w-[32px] xl:hidden" @click="showMenu">
            <div>
              <img src="/assets/icon-menu-open-white.svg" alt="" />
            </div>
          </button>
        </div>
      </div>
    </div>
  </header>

  <!----------------------------scroll up menu----------------------------------->

  <header
    :class="
      ({ '-translate-y-0': scrollUp }, { '-translate-y-full': !scrollUp })
    "
    class="fixed inset-x-0 z-[110] bg-white transition-transform duration-300 top-0"
  >
    <div
      class="w-full px-[24px] mx-auto md:px-[48px] md:max-w-[calc(672px+48px+48px)] xl:max-w-[calc(1290px+48px+48px)] text-black"
    >
      <div class="flex min-h-[64px] items-center justify-between">
        <div class="flex items-center gap-[]">
          <NuxtLink
            to="/"
            class="h-[20px] w-[72px] xl:h-[24px] xl:w-[86px] bg-black"
          >
          </NuxtLink>
        </div>
        <nav class="hidden xl:block">
          <ul class="flex items-center justify-betweeen space-x-[32px]">
            <NuxtLink
              href="/sofunk"
              class="block max-w-max w-full text-center font-500 duration-300 relative border border-transparent bg-transparent"
            >
              <p id="p" v-if="language">So funktioniert's</p>
              <p id="p" v-if="!language">How it works</p>
            </NuxtLink>
            <NuxtLink
              to="/preise"
              class="block max-w-max w-full text-center font-500 duration-300 relative border border-transparent bg-transparent"
            >
              <p id="p" v-if="language">Preise</p>
              <p id="p" v-if="!language">Pricing</p>
            </NuxtLink>
            <NuxtLink
              to="/versicherung"
              class="block max-w-max w-full text-center font-500 duration-300 relative border border-transparent bg-transparent"
              ><p id="p" v-if="language">Versicherung</p>
              <p id="p" v-if="!language">Insurance</p>
            </NuxtLink>
            <NuxtLink
              to="/standorte"
              class="block max-w-max w-full text-center font-500 duration-300 relative border border-transparent bg-transparent"
              ><p id="p" v-if="language">Standorte</p>
              <p id="p" v-if="!language">Locations</p>
            </NuxtLink>
            <div class="relative z-[10] text-left">
              <button
                @click="shownav(), rotate()"
                class="flex items-center space-x-[4px]"
              >
                <span
                  ><p id="p" v-if="language">Mehr</p>
                  <p id="p" v-if="!language">More</p>
                </span>
                <div
                  class="transition-all duration-300"
                  :class="{ ' rotate-[-180deg]': rotate180 }"
                  id="r"
                >
                  <img src="../assets/down-gray.png" class="w-3" />
                </div>
              </button>
              <ul
                v-show="show"
                class="flex flex-col gap-y-[16px] px-[24px] py-[20px] text-gray-900 xl:absolute xl:left-[-32px] xl:mt-2 xl:w-[200px] xl:rounded-[16px] xl:bg-white xl:shadow-xl"
              >
                <li>
                  <NuxtLink to="/">Blutwerte</NuxtLink>
                </li>
                <li>
                  <NuxtLink to="/">Warum CARE?</NuxtLink>
                </li>
                <li>
                  <NuxtLink to="/">Über CARE</NuxtLink>
                </li>
                <li>
                  <NuxtLink to="/">Member Vorteile</NuxtLink>
                </li>
                <li>
                  <NuxtLink to="/">Praxen & Apotheken</NuxtLink>
                </li>
                <li>
                  <NuxtLink to="/">Blog</NuxtLink>
                </li>
              </ul>
            </div>
          </ul>
        </nav>

        <!----------------------------------------------------->

        <div class="flex items-center space-x-[24px] xl:space-x-[16px]">
          <div
            class="bg-blue-600 text-white h-8 rounded-2xl text-sm items-center justify-center text-center py-[6px] px-[12px] font-sans hidden xl:block"
          >
            <a href="https://booking.care.me/ch-de/locations/"
              >Check-up buchen</a
            >
          </div>
          <div class="relative isolate w-max cursor-pointer hidden xl:block">
            <button
              @click="showLgPick"
              class="border rounded-full p-[8px] bg-opacity-0 hover:bg-opacity-20 border-gray-900/20 bg-gray-900 transition-all duration-300"
            >
              <img
                src="../assets/icon-globe-dark.svg"
                class="w-[14px] h-[14px]"
              />
            </button>
            <div
              @click="
                changeEn();
                showLgPick();
              "
              v-show="languageShow"
              class="top-[40px] md:right-0 absolute z-50 w-max rounded-[8px] border border-gray-200 bg-white p-[8px] transition-all duration-300"
            >
              <div
                class="flex w-full cursor-pointer items-center space-x-[8px] rounded-[8px] px-[8px] py-[4px] transition-all duration-300 active:bg-gray-200 hover:bg-gray-100"
              >
                <div
                  v-show="language"
                  class="h-[15px] w-[20px] shrink-0 overflow-hidden inner-img:object-cover rounded-[4px]"
                >
                  <img class="w-full h-full" src="/assets/icon-en-flag.svg" />
                </div>
                <span
                  v-show="language"
                  class="text-[14px] font-500 leading-[21px] tracking-[0.015em] text-gray-900"
                  >English</span
                >
                <div
                  v-show="!language"
                  class="h-[15px] w-[20px] shrink-0 overflow-hidden inner-img:object-cover rounded-[4px]"
                >
                  <img class="w-full h-full" src="/assets/icon-de-flag.svg" />
                </div>
                <span
                  v-show="!language"
                  class="text-[14px] font-500 leading-[21px] tracking-[0.015em] text-gray-900"
                  >Deutsch</span
                >
              </div>
            </div>
          </div>
          <button class="h-[32px] w-[32px] xl:hidden" @click="showMenu">
            <div>
              <img src="/assets/icon-menu-open-white.svg" alt="" />
            </div>
          </button>
        </div>
      </div>
    </div>
  </header>

  <!-- --------------------------Hiden menu--------------------------------- -->
  <div
    v-show="shMenu"
    class="fixed inset-0 z-[120] flex flex-col overflow-y-auto bg-white xl:hidden transition duration-300"
  >
    <div
      class="w-full px-[24px] mx-auto md:px-[48px] md:max-w-[calc(672px+48px+48px)] xl:max-w-[calc(1188px+48px+48px)]"
    >
      <div class="flex h-full grow flex-col py-[16px]">
        <div class="flex justify-between items-center">
          <NuxtLink
            to="/"
            class="h-[20px] w-[72px] xl:h-[24px] xl:w-[86px] bg-black"
          >
          </NuxtLink>
          <button @click="showMenu" class="w-[32px] h-[32px]">
            <div class="w-full h-full">
              <img src="/assets/icon-menu-close-gray-900.svg" alt="" />
            </div>
          </button>
        </div>

        <div class="w-full h-[112px]"></div>

        <div class="flex h-full flex-col items-start justify-between">
          <nav>
            <ul class="flex-cols space-y-[24px] text-gray-900">
              <NuxtLink
                href="/sofunk"
                class="block max-w-max w-full text-center font-medium duration-300 relative border border-transparent bg-transparent text-black text-2xl"
              >
                <p v-if="language">So funktioniert's</p>
                <p v-if="!language">How it works</p>
              </NuxtLink>
              <NuxtLink
                to="/preise"
                class="block max-w-max w-full text-center font-medium duration-300 relative border border-transparent bg-transparent text-black text-2xl"
                >Preise</NuxtLink
              >
              <NuxtLink
                to="/versicherung"
                class="block max-w-max w-full text-center font-medium duration-300 relative border border-transparent bg-transparent text-black text-2xl"
                >Versicherung</NuxtLink
              >
              <NuxtLink
                to="/standorte"
                class="block max-w-max w-full text-center font-medium duration-300 relative border border-transparent bg-transparent text-black text-2xl"
                >Standorte</NuxtLink
              >
              <li>
                <div class="relative z-[10] text-left">
                  <button
                    @click="shownav(), rotate()"
                    class="flex items-center space-x-[4px]"
                  >
                    <span class="text-2xl font-medium xl:text-base">Mehr</span>
                    <div
                      class="transition-all duration-300"
                      :class="{ 'rotate-180': rotate180 }"
                      id="r"
                    >
                      <img src="../assets/icon-up-gray.svg" class="w-3" />
                    </div>
                  </button>
                  <ul
                    v-show="show"
                    class="flex flex-col gap-y-[16px] px-[24px] py-[20px] text-gray-900 focus:outline-none xl:absolute xl:left-[-32px] xl:mt-2 xl:w-[200px] xl:rounded-[16px] xl:bg-white xl:shadow-xl"
                  >
                    <li>
                      <NuxtLink
                        class="block max-w-max w-full text-center font-medium duration-300 relative border border-transparent bg-transparent text-black text-2xl"
                      >
                        Blutwerte
                      </NuxtLink>
                    </li>
                    <li>
                      <NuxtLink
                        class="block max-w-max w-full text-center font-medium duration-300 relative border border-transparent bg-transparent text-black text-2xl"
                      >
                        Warum CARE?
                      </NuxtLink>
                    </li>
                    <li>
                      <NuxtLink
                        class="block max-w-max w-full text-center font-medium duration-300 relative border border-transparent bg-transparent text-black text-2xl"
                      >
                        Über CARE
                      </NuxtLink>
                    </li>
                    <li>
                      <NuxtLink
                        class="block max-w-max w-full text-center font-medium duration-300 relative border border-transparent bg-transparent text-black text-2xl"
                      >
                        Member Vorteile
                      </NuxtLink>
                    </li>
                    <li>
                      <NuxtLink
                        class="block max-w-max w-full text-center font-medium duration-300 relative border border-transparent bg-transparent text-black text-2xl"
                      >
                        Praxen & Apotheken
                      </NuxtLink>
                    </li>
                    <li>
                      <NuxtLink
                        class="block max-w-max w-full text-center font-medium duration-300 relative border border-transparent bg-transparent text-black text-2xl"
                      >
                        Blog
                      </NuxtLink>
                    </li>
                  </ul>
                </div>
              </li>
            </ul>
          </nav>

          <div class="pb-4">
            <div class="w-full h-[30px]"></div>
            <div
              class="relative isolate w-max cursor-pointer mt-auto"
              @click="
                rotateLg();
                showLgPick();
              "
            >
              <div
                class="relative flex w-max items-center rounded-full border bg-opacity-0 transition-all duration-300 hover:bg-opacity-20 border-gray-900/20 bg-gray-900 text-gray-900 px-[12px] py-[6px]"
              >
                <div class="h-[14px] w-[14px]">
                  <img src="/assets/icon-globe-dark.svg" alt="" />
                </div>
                <p class="mx-[4px] text-xs">Deutsch</p>
                <div>
                  <div
                    class="transition-all duration-300 rotate-180"
                    :class="{ 'rotate-0': rotate0 }"
                    id="r"
                  >
                    <img src="../assets/icon-up-gray.svg" class="w-3" />
                  </div>
                </div>
              </div>
              <div
                @click="changeEn"
                v-show="languageShow"
                class="bottom-[40px] md:right-0 absolute z-50 w-max rounded-[8px] border border-gray-200 bg-white p-[8px] transition-all duration-300"
              >
                <div
                  class="flex w-full cursor-pointer items-center space-x-[8px] rounded-[8px] px-[8px] py-[4px] transition-all duration-300 active:bg-gray-200 hover:bg-gray-100"
                >
                  <div
                    v-show="language"
                    class="h-[15px] w-[20px] shrink-0 overflow-hidden inner-img:object-cover rounded-[4px]"
                  >
                    <img class="w-full h-full" src="/assets/icon-en-flag.svg" />
                  </div>
                  <span
                    v-show="language"
                    class="text-[14px] font-500 leading-[21px] tracking-[0.015em] text-gray-900"
                    >English</span
                  >
                  <div
                    v-show="!language"
                    class="h-[15px] w-[20px] shrink-0 overflow-hidden inner-img:object-cover rounded-[4px]"
                  >
                    <img class="w-full h-full" src="/assets/icon-de-flag.svg" />
                  </div>
                  <span
                    v-show="!language"
                    class="text-[14px] font-500 leading-[21px] tracking-[0.015em] text-gray-900"
                    >Deutsch</span
                  >
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- ----------------------------------------------------------- -->

  <div>
    <slot />
  </div>

  <footer>
    <div class="relative bg-neutral-900 py-[48px] md:py-[64px] xl:py-[128px]">
      <div style="padding: 0 174px; margin: 0 auto; max-width: 1536px">
        <div class="flex space-x-[120px]">
          <div class="col-span-4 space-y-[24px] md:col-span-8 xl:col-span-4">
            <div
              class="h-[20px] w-[72px] xl:h-[24px] xl:w-[86px] bg-white"
            ></div>
            <p class="text-gray-300 xl:max-w-[277px] text-base">
              CARE unterstützt Menschen dabei, ihre Gesundheit besser zu
              verstehen, um ein gesünderes und längeres Leben zu führen.
            </p>
          </div>
          <nav
            class="col-span-4 space-y-[32px] py-[32px] md:col-span-8 md:grid md:grid-cols-8 md:space-y-0 md:pb-[48px] md:pt-[32px] xl:grid-cols-8 xl:gap-x-[24px] xl:py-0"
          >
            <div class="col-span-4 space-y-[24px] md:col-span-8 xl:col-span-4">
              <div class="space-y-[24px] text-white">
                <h3 class="text-2xl font-semibold">Links</h3>
                <ul class="space-y-[16px]">
                  <li>So funktioniert's</li>
                  <li>Preise</li>
                  <li>Warum Blutanalyse?</li>
                  <li>Blutwerte</li>
                  <li>Versicherung</li>
                  <li>Blog</li>
                </ul>
              </div>
            </div>
          </nav>
          <nav
            class="col-span-4 space-y-[32px] py-[32px] md:col-span-8 md:grid md:grid-cols-8 md:space-y-0 md:pb-[48px] md:pt-[32px] xl:grid-cols-8 xl:gap-x-[24px] xl:py-0"
          >
            <div class="col-span-4 space-y-[24px] md:col-span-8 xl:col-span-4">
              <div class="space-y-[24px] text-white">
                <h3 class="text-2xl font-semibold">Unternehmen</h3>
                <ul class="space-y-[16px]">
                  <li>Warum CARE</li>
                  <li>Über CARE</li>
                  <li>Member Vorteile</li>
                  <li>Für Praxen & Apotheken</li>
                  <li>Standorte</li>
                  <li>Jobs</li>
                </ul>
              </div>
            </div>
          </nav>
        </div>

        <div
          class="col-span-4 space-y-[32px] border-y border-neutral-800 py-[48px] md:col-span-8 md:flex md:items-center md:justify-between md:space-y-0 md:py-[50px] xl:col-start-1 xl:col-end-13 xl:mb-[32px] xl:mt-[64px] xl:py-[26px]"
        >
          <h3 class="text-2xl text-white font-bold">
            Jetzt vom App Store herunterladen
          </h3>
        </div>
        <p class="text-white">© 2024 CARE. Alle Rechte vorbehalten.</p>
      </div>
    </div>
  </footer>
</template>

<script setup>
import { ref } from "vue";
var languageShow = ref(false);
var show = ref(false);
var rotate180 = ref(false);
var rotate0 = ref(false);
var language = ref(true);
var shMenu = ref(false);
var scrollPosition = ref();
var scrollUp = ref(false);

function shownav() {
  show.value = !show.value;
}
function rotate() {
  rotate180.value = !rotate180.value;
}
function rotateLg() {
  rotate0.value = !rotate0.value;
}
function showLgPick() {
  languageShow.value = !languageShow.value;
}
function changeEn() {
  language.value = !language.value;
}
function showMenu() {
  shMenu.value = !shMenu.value;
}

onMounted(() => {
  window.addEventListener("scroll", handleScroll);
});

function handleScroll() {
  if (scrollPosition > window.scrollY && window.scrollY > 100) {
    scrollUp.value = true;
    console.log(scrollUp);
  } else {
    scrollUp.value = false;
    console.log(scrollUp);
  }
  scrollPosition = window.scrollY;
}
</script>
