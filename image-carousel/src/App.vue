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
        <div class="absolute inset-10 p-10 flex items-end">
          <div
            class="w-fit bg-zinc-800/30 backdrop-blur-lg rounded-lg ring-2 ring-zinc-50/30 p-10">
            <h1 class="text-4xl font-bold text-white">Flicking</h1>
            <p class="text-xl text-zinc-300 py-2">
              Lorem ipsum dolor sit amet, consectetur adipisicing elit. Fugit
              sit soluta commodi et labore non! Veniam at voluptate porro
              delectus harum sit? Vero necessitatibus dicta labore quia
              temporibus, ex exercitationem.
            </p>
          </div>
        </div>
      </div>
      <div class="h-full flex items-center justify-center relative">
        <img
          class="max-w-[90%] max-h-[90%] rounded-2xl shadow-2xl"
          src="./assets/2.png"
          alt=""
          draggable="false" />
          <div class="absolute inset-10 p-10 flex items-end">
            <div
              class="w-fit bg-zinc-800/30 backdrop-blur-lg rounded-lg ring-2 ring-zinc-50/30 p-10">
              <h1 class="text-4xl font-bold text-white">Flicking</h1>
              <p class="text-xl text-zinc-300 py-2">
                Lorem ipsum dolor sit amet, consectetur adipisicing elit. Fugit
                sit soluta commodi et labore non! Veniam at voluptate porro
                delectus harum sit? Vero necessitatibus dicta labore quia
                temporibus, ex exercitationem.
              </p>
            </div>
          </div>
      </div>
      <div class="h-full flex items-center justify-center relative">
        <img
          class="max-w-[90%] max-h-[90%] rounded-2xl shadow-2xl"
          src="./assets/3.png"
          alt=""
          draggable="false" />
          <div class="absolute inset-10 p-10 flex items-end">
            <div
              class="w-fit bg-zinc-800/30 backdrop-blur-lg rounded-lg ring-2 ring-zinc-50/30 p-10">
              <h1 class="text-4xl font-bold text-white">Image 3</h1>
            </div>
          </div>
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
</style>
