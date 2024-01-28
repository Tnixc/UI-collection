<template>
  <body class="flex h-screen flex-col items-center bg-white">
    <h1 class="text-balance pt-52 text-center text-8xl font-bold text-zinc-800">
      <span>Sphinx &nbsp;</span>
      <span>of &nbsp;</span>
      <span>black &nbsp;</span>
      <span>quartz</span>
    </h1>
    <h2 class="text-5xl text-zinc-400 pt-20">
      judge my vow
    </h2>
    <div class="absolute bottom-0 left-28 right-28 h-96" id="gradient"></div>
  </body>
</template>
<style>
body {
  font-family: "Aptos";
}
@keyframes popup {
  0% {
    transform: scale(1) translateY(0);
    filter: blur(5px);
    opacity: 0;
  }
  50% {
    transform: scale(1) translateY(-1%);
    filter: blur(2.5px);
    opacity: 0.1;
  }
  100% {
    transform: scale(1) translateY(0);
    filter: blur(0px);
    opacity: 1;
  }
}
span {
  display: inline-block;
  opacity: 0;
  transform: scale(0.9) translateY(0);
  animation: popup 0.7s cubic-bezier(0.175, 0.885, 0.32, 1.275);
  animation-fill-mode: forwards;
  &:nth-child(1) {
    animation-delay: 0.2s;
  }
  &:nth-child(2) {
    animation-delay: 0.4s;
  }
  &:nth-child(3) {
    animation-delay: 0.6s;
  }
  &:nth-child(4) {
    animation-delay: 0.8s;
  }
}
@keyframes fade {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
h2 {
  animation: fade 1s cubic-bezier(0.175, 0.885, 0.32, 1.275);
  animation-fill-mode: forwards;
  animation-delay: 1.5s;
  opacity: 0;
}
#gradient {
  background-image: linear-gradient(to top, #fbc2eb 0%, #a6c1ee 100%);
  filter: blur(50px);
}
</style>
