<script setup>
import { RouterLink } from "vue-router";
import { onMounted } from "vue";
const emit = defineEmits([
  "footerLoaded",
  "main-swiper--prev",
  "main-swiper--next",
]);

onMounted(() => {
  emit("footerLoaded");
});
</script>

<template>
  <header
    class="footer-nav | border-t border-t-zinc-950 | fixed w-full bottom-0 | bg-white"
  >
    <div
      class="footer-nav--wrapper | grid grid-cols-3 gap-4 grid-flow-row | w-full mx-auto"
    >
      <div class="grid items-stretch justify-start">
        <button
          class="footer-btn footer-btn--prev | p-4 transition-all duration-75 hover:bg-zinc-950 hover:text-white active:bg-zinc-700 active:text-white"
          @click="$emit('main-swiper--prev')"
        >
          <svg
            xmlns="http://www.w3.org/2000/svg"
            fill="none"
            viewBox="0 0 24 24"
            stroke-width="1"
            stroke="currentColor"
            class="w-16 h-16"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              d="M10.5 19.5L3 12m0 0l7.5-7.5M3 12h18"
            />
          </svg>
        </button>
      </div>
      <div class="grid | items-stretch justify-center">
        <button
          class="bg-zinc-950 text-white text-lg xl:text-2xl | transition-all duration-75 hover:bg-zinc-800 | p-4 xl:p-10"
        >
          Book a Consultation
        </button>
      </div>
      <div class="grid items-stretch justify-end">
        <button
          class="footer-btn footer-btn--next | p-4 | transition-all duration-75 hover:bg-zinc-950 hover:text-white active:bg-zinc-700 active:text-white"
          @click="$emit('main-swiper--next')"
        >
          <svg
            xmlns="http://www.w3.org/2000/svg"
            fill="none"
            viewBox="0 0 24 24"
            stroke-width="1"
            stroke="currentColor"
            class="w-16 h-16"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              d="M13.5 4.5L21 12m0 0l-7.5 7.5M21 12H3"
            />
          </svg>
        </button>
      </div>
    </div>
  </header>
</template>

<style scoped lang="scss"></style>
