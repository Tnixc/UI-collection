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
      class="rounded-3xl h-full shadow-inner bg-gradient-to-br from-neutral-200 to-neutral-300 ring-4 ring-zinc-50"
      id="Flicking"
      :options="{ circular: true, moveType: 'snap' }"
      :viewportTag="'div'"
      :cameraTag="'div'">
      <div class="h-full flex items-center justify-center">
        <img
          class="max-w-[90%] max-h-[90%] rounded-2xl shadow-2xl"
          src="./assets/1.png"
          alt=""
          draggable="false" />
      </div>
      <div class="h-full flex items-center justify-center">
        <img
          class="max-w-[90%] max-h-[90%] rounded-2xl shadow-2xl"
          src="./assets/2.png"
          alt=""
          draggable="false" />
      </div>
      <div class="h-full flex items-center justify-center">
        <img
          class="max-w-[90%] max-h-[90%] rounded-2xl shadow-2xl"
          src="./assets/3.png"
          alt=""
          draggable="false" />
      </div>
      <div class="h-full flex items-center justify-center">
        <img
          class="max-w-[90%] max-h-[90%] rounded-2xl shadow-2xl"
          src="./assets/4.png"
          alt=""
          draggable="false" />
      </div>
      <div class="h-full flex items-center justify-center">
        <img
          class="max-w-[90%] max-h-[90%] rounded-2xl shadow-2xl"
          src="./assets/5.png"
          alt=""
          draggable="false" />
      </div>
      <div class="h-full flex items-center justify-center">
        <img
          class="max-w-[90%] max-h-[90%] rounded-2xl shadow-2xl"
          src="./assets/6.png"
          alt=""
          draggable="false" />
      </div>
    </Flicking>
  </body>
</template>
<style></style>
