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
      <div class=" bg-slate-800">
        <img src="./assets/1.png" alt="1" draggable="false" />
      </div>
      <div class=" bg-slate-800">
        <img src="./assets/2.png" alt="2" draggable="false" />
      </div>
      <div class=" bg-slate-800">
        <img src="./assets/3.png" alt="3" draggable="false" />
      </div>
      <div class=" bg-slate-800">
        <img src="./assets/4.png" alt="4" draggable="false" />
      </div>
      <div class=" bg-slate-800">
        <img src="./assets/5.png" alt="5" draggable="false" />
      </div>
      <div class=" bg-slate-800">
        <img src="./assets/6.png" alt="6" draggable="false" />
      </div>
    </Flicking>
  </body>
</template>
<style>

</style>
