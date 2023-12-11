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
  <div class="flex items-center justify-center p-40 h-screen bg-black">
    <div class="relative w-full h-full overflow-hidden">
      <Mocha class="absolute inset-0 shadow-2xl" id="Mocha"/>
      <Macchiato class="absolute inset-0 shadow-2xl" id="Macchiato"/>
      <Frappe class="absolute inset-0 shadow-2xl" id="Frappe"/>
      <Latte class="absolute inset-0 shadow-2xl" id="Latte"/>
    </div>
  </div>
</template>
<style scoped>
#Latte{
  animation: Latte cubic-bezier(0.175, 0.885, 0.32, 1) 2s;
  clip-path: polygon(0 0, 25% 0, 25% 100%, 0 100%);

}
#Frappe{
  animation: Frappe cubic-bezier(0.175, 0.885, 0.32, 1) 3s;
  clip-path: polygon(0 0, 50% 0, 50% 100%, 0 100%);

}
#Macchiato{
  animation: Macchiato cubic-bezier(0.175, 0.885, 0.32, 1) 5s;
  clip-path: polygon(0 0, 75% 0, 75% 100%, 0 100%);
}
@keyframes Latte {
  0% {
    clip-path: polygon(0 0, 100% 0, 100% 100%, 0 100%);
  }
  100% {
    clip-path: polygon(0 0, 25% 0, 25% 100%, 0 100%);
  }
}
@keyframes Frappe {
  0% {
    clip-path: polygon(0 0, 100% 0, 100% 100%, 0 100%);
  }
  100% {
    clip-path: polygon(0 0, 50% 0, 50% 100%, 0 100%);
  }
}
@keyframes Macchiato {
  0% {
    clip-path: polygon(0 0, 100% 0, 100% 100%, 0 100%);
  }
  100% {
    clip-path: polygon(0 0, 75% 0, 75% 100%, 0 100%);
  }
}
</style>