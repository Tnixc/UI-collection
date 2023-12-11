<script lang="ts">
import { ref } from "vue";
import "@egjs/vue3-flicking/dist/flicking.css";
import Flicking from "@egjs/vue3-flicking";

export default {
  name: "YourComponent",
  components: {
    Flicking,
  },
  setup() {
    const flicking = ref(null);
    const goToPrevious = () => {
      if (flicking.value) {
        (flicking.value as any).prev();
      }
    };
    const goToNext = () => {
      if (flicking.value) {
        (flicking.value as any).next();
      }
    };

    return {
      flicking,
      goToPrevious,
      goToNext,
    };
  },
};
</script>

<template>
  <body
    class="flex h-[98vh] flex-col items-center justify-center bg-neutral-100 p-32 pt-10"
  >
    <Flicking
      ref="flicking"
      class="relative h-full w-full rounded-3xl bg-gradient-to-br from-neutral-200 to-neutral-300 shadow-inner ring-4 ring-zinc-50"
      id="Flicking"
      :options="{
        circular: true,
      }"
      :viewportTag="'div'"
      :cameraTag="'div'"
    >
      <div class="relative flex h-full max-w-full items-center justify-center">
        <img
          class="max-h-[90%] max-w-[90%] rounded-2xl shadow-2xl"
          src="./assets/1.png"
          alt=""
          draggable="false"
        />
      </div>
      <div class="relative flex h-full max-w-full items-center justify-center">
        <img
          class="max-h-[90%] max-w-[90%] rounded-2xl shadow-2xl"
          src="./assets/2.png"
          alt=""
          draggable="false"
        />
      </div>
      <div class="relative flex h-full max-w-full items-center justify-center">
        <img
          class="max-h-[90%] max-w-[90%] rounded-2xl shadow-2xl"
          src="./assets/3.png"
          alt=""
          draggable="false"
        />
      </div>
      <div class="relative flex h-full max-w-full items-center justify-center">
        <img
          class="max-h-[90%] max-w-[90%] rounded-2xl shadow-2xl"
          src="./assets/4.png"
          alt=""
          draggable="false"
        />
      </div>
      <div class="relative flex h-full max-w-full items-center justify-center">
        <img
          class="max-h-[90%] max-w-[90%] rounded-2xl shadow-2xl"
          src="./assets/5.png"
          alt=""
          draggable="false"
        />
      </div>
      <div class="relative flex h-full max-w-full items-center justify-center">
        <img
          class="max-h-[90%] max-w-[90%] rounded-2xl shadow-2xl"
          src="./assets/6.png"
          alt=""
          draggable="false"
        />
      </div>
    </Flicking>
    <div class="flex items-center justify-center gap-3 p-4">
      <button class="rounded-full bg-zinc-200 p-4 text-4xl aspect-square flex items-center" @click="goToPrevious">
        ←
      </button>
      <span class="text-2xl">Current index</span><span></span>
      <button class="rounded-full bg-zinc-200 p-4 text-4xl aspect-square flex items-center " @click="goToNext">
        →
      </button>
    </div>
  </body>
  <a
    href="https://www.behance.net/gallery/184542573/PimBank-UXUI-Design?tracking_source=search_projects&l=1"
    >Image sources:
    https://www.behance.net/gallery/184542573/PimBank-UXUI-Design?tracking_source=search_projects&l=1</a
  >
</template>
<style>
#Flicking::after {
  content: "";
  position: absolute;
  inset: 0;
  background: linear-gradient(
    to right,
    #f5f5f54a,
    #f5f5f500,
    #f5f5f500,
    #f5f5f500,
    #f5f5f54a
  );
  z-index: 9;
  opacity: 20%;
}
#Flicking::before {
  content: "";
  position: absolute;
  inset: 0;
  box-shadow: inset 0 0 0 7px #f5f5f54a;
  z-index: 99;
  border-radius: 1.5rem;
}
@keyframes widen {
  0% {
    width: 90%;
  }
  100% {
    width: 100%;
  }
}
#Flicking {
  animation: widen 0.5s ease-in-out;
}
</style>
