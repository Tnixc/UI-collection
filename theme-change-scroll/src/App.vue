<script lang="ts">
import Latte from "./components/Latte.vue";
import Frappe from "./components/Frappe.vue";
import Macchiato from "./components/Macchiato.vue";
import Mocha from "./components/Mocha.vue";
export default {
  components: {
    Latte,
    Frappe,
    Macchiato,
    Mocha,
  },
};
</script>
<template>
  <div class="flex items-center justify-center p-40 h-screen">
    <div class="relative w-full h-full">
      <Mocha class="absolute inset-0" id="Mocha"/>
      <Macchiato class="absolute inset-0" id="Macchiato"/>
      <Frappe class="absolute inset-0" id="Frappe"/>
      <Latte class="absolute inset-0" id="Latte"/>
    </div>
  </div>
</template>
<style scoped>
</style>