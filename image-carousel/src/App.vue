<script lang="ts">
import Flicking from "@egjs/vue3-flicking";
import "@egjs/flicking/dist/flicking.css";
export default {
  components: {
    Flicking,
  },
};
</script>
<template>
  <body
    class="h-[98vh] flex items-center justify-center bg-neutral-100 p-32 pt-10"
  >
    <Flicking
      class="rounded-3xl h-full shadow-inner bg-gradient-to-br from-neutral-200 to-neutral-300 ring-4 ring-zinc-50 relative w-full"
      id="Flicking"
      :options="{
        circular: true,
        defaultIndex: 1,
      }"
      :viewportTag="'div'"
      :cameraTag="'div'"
    >
      <div class="h-full flex items-center justify-center relative max-w-full">
        <img
          class="max-w-[90%] max-h-[90%] rounded-2xl shadow-2xl"
          src="./assets/1.png"
          alt=""
          draggable="false"
        />
      </div>
      <div class="h-full flex items-center justify-center relative max-w-full">
        <img
          class="max-w-[90%] max-h-[90%] rounded-2xl shadow-2xl"
          src="./assets/2.png"
          alt=""
          draggable="false"
        />
      </div>
      <div class="h-full flex items-center justify-center relative max-w-full">
        <img
          class="max-w-[90%] max-h-[90%] rounded-2xl shadow-2xl"
          src="./assets/3.png"
          alt=""
          draggable="false"
        />
      </div>
      <div class="h-full flex items-center justify-center relative max-w-full">
        <img
          class="max-w-[90%] max-h-[90%] rounded-2xl shadow-2xl"
          src="./assets/4.png"
          alt=""
          draggable="false"
        />
      </div>
      <div class="h-full flex items-center justify-center relative max-w-full">
        <img
          class="max-w-[90%] max-h-[90%] rounded-2xl shadow-2xl"
          src="./assets/5.png"
          alt=""
          draggable="false"
        />
      </div>
      <div class="h-full flex items-center justify-center relative max-w-full">
        <img
          class="max-w-[90%] max-h-[90%] rounded-2xl shadow-2xl"
          src="./assets/6.png"
          alt=""
          draggable="false"
        />
      </div>
    </Flicking>
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
  @apply rounded-3xl;
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
