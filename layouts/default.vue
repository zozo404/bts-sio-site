<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <div class="selection:bg-cyan-500 selection:text-black">
    <Header />
    <nuxt />
    <Footer />
  </div>
</template>
<script>
export default {
  name: 'DefaultLayout'
}
</script>
<style>
html{
  font-family: 'Comfortaa';
}
.fade-scroll {
  opacity: 0;
  transition: opacity 0.5s ease-in-out;
}
.fade-scroll.visible {
  opacity: 1;
}
.flex-di-initial{
  flex-direction: initial;
}
/* Container de la barre */
::-webkit-scrollbar {
    width: 14px;
}

/* Track (Le fond de la barre) */
::-webkit-scrollbar-track {
    background: #000000;
}

/* Handle (La partie mobile) */
::-webkit-scrollbar-thumb {
    background: #fb923c;
    border-radius: 1rem;
    border: 2px solid #000000;
}

/* Handle au survol */
::-webkit-scrollbar-thumb:hover {
    background: #f97316;
    cursor: pointer;
}
</style>
