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
  <body class="h-screen flex items-center justify-center bg-neutral-100 p-20">
    <Flicking
      class="rounded-3xl h-full shadow-inner bg-gradient-to-br from-neutral-200 to-neutral-300 ring-4 ring-zinc-50 relative"
      id="Flicking"
      :options="{ circular: true, moveType: 'snap' }"
      :viewportTag="'div'"
      :cameraTag="'div'">
      <div class="h-full flex items-center justify-center relative">
        <img
          class="max-w-[90%] max-h-[90%] rounded-2xl shadow-2xl"
          src="./assets/1.png"
          alt=""
          draggable="false" />
        <div class="absolute inset-10 p-10 bg-red-400/30 flex items-end">
          <div class="w-fit bg-teal-400/30 p-10">
            <h1 class="text-4xl font-bold text-white">Flicking</h1>
            <p class="text-xl text-white">A flexible, customizable, touch-friendly carousel for Vue3</p>
          </div>
        </div>
      </div>
      <div class="h-full flex items-center justify-center relative">
        <img
          class="max-w-[90%] max-h-[90%] rounded-2xl shadow-2xl"
          src="./assets/2.png"
          alt=""
          draggable="false" />
      </div>
      <div class="h-full flex items-center justify-center relative">
        <img
          class="max-w-[90%] max-h-[90%] rounded-2xl shadow-2xl"
          src="./assets/3.png"
          alt=""
          draggable="false" />
      </div>
      <div class="h-full flex items-center justify-center relative">
        <img
          class="max-w-[90%] max-h-[90%] rounded-2xl shadow-2xl"
          src="./assets/4.png"
          alt=""
          draggable="false" />
      </div>
      <div class="h-full flex items-center justify-center relative">
        <img
          class="max-w-[90%] max-h-[90%] rounded-2xl shadow-2xl"
          src="./assets/5.png"
          alt=""
          draggable="false" />
      </div>
      <div class="h-full flex items-center justify-center relative">
        <img
          class="max-w-[90%] max-h-[90%] rounded-2xl shadow-2xl"
          src="./assets/6.png"
          alt=""
          draggable="false" />
      </div>
    </Flicking>
  </body>
</template>
<style>
#Flicking::after{
  content: "";
  position: absolute;
  inset: 0;
  background: linear-gradient(to right, #f5f5f54a, #F5F5F500,#F5F5F500, #F5F5F500, #F5F5F54a);
  z-index: 9;
  opacity: 20%;
}
#Flicking::before{
  content: "";
  position: absolute;
  inset: 0;
  box-shadow: inset 0 0 0 7px #f5f5f54a;
  z-index: 99;
  @apply rounded-3xl;
}
</style>
