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
  <body class="h-screen flex items-center justify-center bg-neutral-900 p-20">
    <Flicking
      class="ring-red-300 ring-4 h-full"
      id="Flicking"
      :options="{ circular: true, moveType: 'snap' }"
      :viewportTag="'div'"
      :cameraTag="'div'">
    <div class="h-full bg-gradient-to-r from-teal-400 to-white flex items-center">
      <img class="scale-90 max-h-[95%]" src="./assets/1.png" alt="" draggable="false">
    </div>
    <div class="h-full bg-gradient-to-r from-teal-400 to-white flex items-center">
      <img class="scale-90 max-h-[95%]" src="./assets/2.png" alt="" draggable="false">
    </div>
    <div class="h-full bg-gradient-to-r from-teal-400 to-white flex items-center">
      <img class="scale-90 max-h-[95%]" src="./assets/3.png" alt="" draggable="false">
    </div>
    </Flicking>
  </body>
</template>
<style>
</style>
