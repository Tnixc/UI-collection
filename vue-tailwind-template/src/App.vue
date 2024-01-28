<template>
  <body class="bg-white h-screen flex items-center flex-col">
    <h1 class="text-zinc-800 text-8xl font-bold text-center text-balance py-52">
      <span>Where &nbsp;</span>
      <span>knowledge &nbsp;</span>
      <span>begins</span>
    </h1>
  </body>
</template>
<style>
@keyframes popup{
  0%{
    transform: scale(1) translateY(0);
    filter: blur(5px);
    opacity: 0;
  }
  50%{
    transform: scale(1) translateY(-3%);
    filter: blur(2.5px);
    opacity: 0.1;
  }
  100%{
    transform: scale(1) translateY(0);
    filter: blur(0px);
    opacity: 1;
  }
}
span{
  display: inline-block;
  opacity: 0;
  transform: scale(0.9) translateY(0);
}
span{
  animation: popup 1s cubic-bezier(0.175, 0.885, 0.32, 1.275);
  animation-fill-mode: forwards;
}
span:nth-child(1){
  animation-delay: 0.3s;
}
span:nth-child(2){
  animation-delay: 0.6s;
}
span:nth-child(3){
  animation-delay: 0.9s;
}

</style>