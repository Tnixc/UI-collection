<script lang="ts">
import Flicking from "@egjs/vue3-flicking";
import "@egjs/flicking/dist/flicking.css";
export default {
  components: {
    Flicking
  }
}
</script>
<template>
  <Flicking class=" m-20 w-40 h-40">
  <!-- <Flicking :options="{ circular: true }"> -->
    <div class="panel h-40 w-40 bg-red-400">Panel 1</div>
    <div class="panel h-40 w-40 bg-blue-400">Panel 2</div>
    <div class="panel h-40 w-40 bg-emerald-400">Panel 3</div>
  </Flicking>
</template>