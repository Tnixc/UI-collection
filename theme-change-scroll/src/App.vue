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
      <Mocha class="absolute inset-0" id="Mocha"/>
      <Macchiato class="absolute inset-0" id="Macchiato"/>
      <Frappe class="absolute inset-0" id="Frappe"/>
      <Latte class="absolute inset-0" id="Latte"/>
    </div>
  </div>
</template>
<style scoped>
#Latte{
  animation: Latte cubic-bezier(0.175, 0.885, 0.32, 1) 5s;
  clip-path: polygon(0 0, 33.3333% 0, 0 100%, 0 100%);

}
#Frappe{
  animation: Frappe cubic-bezier(0.175, 0.885, 0.32, 1) 8s;
  clip-path: polygon(0 0, 66% 0, 33% 100%, 0 100%);

}
#Macchiato{
  animation: Macchiato cubic-bezier(0.175, 0.885, 0.32, 1) 12s;
  clip-path: polygon(0 0, 100% 0, 66% 100%, 0 100%);
}
@keyframes Latte {
  from {
    clip-path: polygon(0 0, 100% 0, 100% 100%, 0% 100%);
  }
  to {
    clip-path: polygon(0 0, 33.3333% 0, 0 100%, 0 100%);
  }
}
@keyframes Frappe {
  from {
    clip-path: polygon(0 0, 100% 0, 100% 100%, 0% 100%);
  }
  to {
    clip-path: polygon(0 0, 66% 0, 33% 100%, 0 100%);
  }
}
@keyframes Macchiato {
  from {
    clip-path: polygon(0 0, 100% 0, 100% 100%, 0% 100%);
  }
  to {
    clip-path: polygon(0 0, 100% 0, 66% 100%, 0 100%);
  }
}
</style>